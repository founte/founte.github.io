\#include \<stdio.h\>

\#include \<stdlib.h\>

\#include \<time.h\>

\#include \<string.h\>

\#include \<string\>

\#include \<iostream\>

using namespace std;

//str : 20201030

int time2unix(string str)

{

struct tm time;

time_t t;

if (str.length() != 8)

return 0;

time.tm_year = atoi(str.substr(0, 4).c_str()) - 1900; /\* 年份修正 \*/

time.tm_mon = atoi(str.substr(4, 2).c_str()) - 1; /\* 月份修正 \*/

time.tm_mday = atoi(str.substr(6, 2).c_str());

time.tm_hour = 0;

time.tm_min = 0;

time.tm_sec = 0;

t = mktime(&time);

return (int)t;

}

string unix2time(int n, int format)

{

char s[100] = { 0 };

memset(s, 0, 100);

time_t tick = (time_t)(n);

struct tm\* tm = localtime(&tick);

switch (format)

{

case TIEM_TYPE_DATE: //DATA: 20201030

strftime(s, sizeof(s), "%Y%m%d", tm);

break;

default: //TIME: 2020-10-30 10:10:10

strftime(s, sizeof(s), "%Y-%m-%d %H:%M:%S", tm);

break;

}

return string(s);

}

int main()

{

string ret;

string str = "20200131";

int a = 0;

a = time2unix(str);

cout \<\< a \<\< endl;

if (a == 0)

ret = unix2time(a);

else

{

a += 86400;

ret = unix2time(a);

}

cout \<\< ret \<\< endl;

}
