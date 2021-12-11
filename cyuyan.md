\#include <stdio.h>

\#include <string.h>

\#define MAX_SIZE 10

struct stu

{

​	long num;

​	char name[20];

​	float score;

​	struct stu *next;

};

int main(void)

{

​	struct stu a[MAX_SIZE];

​	void *head;

​	struct stu *p;

​	a[0].num=202102913;

​	strcpy(a[0].name,"朱龙桓");

​	a[0].score=90.5;

​	a[1].num=202102911;

​	strcpy(a[1].name,"赵旭彰");

​	a[1].score=89.0;

​	a[2].num=202102914;

​	strcpy(a[2].name,"朱蕊宏");

​	a[2].score=92.5;

​	a[3].num=202102910;

​	strcpy(a[3].name,"赵舜舜");

​	a[3].score=90.5;

​	a[0].next=&a[1];

​	a[1].next=&a[2];

​	a[2].next=&a[3];

​	a[3].next=NULL;

​	head=&a;

​	p=(struct stu *)head;

​	do

​	{  printf("num=%ld,name=%s,score=%0.1f\n",p->num,p->name,p->score);	

​		p=p->next;

​	}

​	while(p!=NULL);

​	return 0;

}

