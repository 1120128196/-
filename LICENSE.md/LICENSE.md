#include<stdio.h>
#include<stdlib.h>
#include<math.h>
#include<iostream>

int main()
{//���� 
  int x=0,y,biryear,birmon,birday,year,mon,day,number1=0,number2=0,a=0,t,q,z;
 
	 printf("--------------------------------------\n");
     printf("|      ��������������ڲ�ѯ          |\n");
     printf("|           1:��ʼ��ѯ               |\n");
     printf("|           2:�˳�����               |\n");
     printf("--------------------------------------\n");
     scanf("%d",&y);

  
  if(y!=2)
   {
	  printf("��������ĳ���_��_��_��\n");
      scanf("%d %d %d",&biryear,&birmon,&birday);
      getchar();
      printf("��������Ĳ��Ե�����_��_��_��\n");
      scanf("%d %d %d",&year,&mon,&day);
  
   
 //������ 
	if((biryear%4==0&&biryear%100!=0)||(biryear%400==0))
	{
		switch(birmon)
		{
		case 1 :number1=0;break;
		case 2 :number1=31;break;
		case 3 :number1=60;break;
		case 4 :number1=91;break;
		case 5 :number1=121;break;
		case 6 :number1=152;break;
		case 7 :number1=182;break;
		case 8 :number1=213;break;
		case 9 :number1=244;break;
		case 10:number1=274;break;
		case 11:number1=305;break;
		case 12:number1=335;break;
		}
		number1=number1+birday;
	}
	else
	{
		switch(birmon)
		{
		case 1 :number1=0;break;
		case 2 :number1=31;break;
		case 3 :number1=60;break;
		case 4 :number1=91;break;
		case 5 :number1=121;break;
		case 6 :number1=152;break;
		case 7 :number1=182;break;
		case 8 :number1=213;break;
		case 9 :number1=244;break;
		case 10:number1=274;break;
		case 11:number1=305;break;
		case 12:number1=335;break;
		}
		number1=number1+birday;
	}
		if((year%4==0&&year%100!=0)||(year%400==0))
	{
		switch(mon)
		{
		case 1 :number2=0;break;
		case 2 :number2=31;break;
		case 3 :number2=60;break;
		case 4 :number2=91;break;
		case 5 :number2=121;break;
		case 6 :number2=152;break;
		case 7 :number2=182;break;
		case 8 :number2=213;break;
		case 9 :number2=244;break;
		case 10:number2=274;break;
		case 11:number2=305;break;
		case 12:number2=335;break;
		}
		number2=number2+day;
	}
	else
	{
		switch(mon)
		{
		case 1 :number2=0;break;
		case 2 :number2=31;break;
		case 3 :number2=60;break;
		case 4 :number2=91;break;
		case 5 :number2=121;break;
		case 6 :number2=152;break;
		case 7 :number2=182;break;
		case 8 :number2=213;break;
		case 9 :number2=244;break;
		case 10:number2=274;break;
		case 11:number2=305;break;
		case 12:number2=335;break;
		}
		number2=number2+day;
	}
		for(biryear;biryear<=year;biryear++)
		{
			if((biryear%4==0&&biryear%100!=0)||(biryear%400==0))
		
				a=a+1;
		}
		x=((year-biryear)*365+a-number1+number2)*-1;
		
	  //�ܺ��� 
	char t=0,q=0,z=0;
	t=x%23;
	q=x%28;
	z=x%33;
	//������������ 
	if(t==0)
	{
	  printf("�������������ɵ�������,��ʱ�����������½�,�������������\n");
	}
	else if(t>0&&t<12)
	{
		printf("�������������ɵĸ߳��ڵĵ�%d��,��ͨȺ�ڿ����ڴ��ڼ�úý����������˶�Ա��ɼ�ǿ���ʱ���ѵ�����Ա�ﵽ���õ�ѵ��Ч��\n",t);	
	}
	else if(t==12)
	{
	    printf("�������������ɵ��ٽ��գ��������Σ�ջ����������ķ���\n");
	}
	else if(t>12)
	{
		printf("�������������ɵĵͳ��ڣ����ڼ���ò�Ҫ���������Σ�ջ�����Լ���������һ������\n");
	}
	//������������ 
	if(q==0)
	{
        printf("�������������ɵ�������\n");
	}
	else if(q>0&&q<14)
	{
		printf("�������������ɸ߳��ڵĵ�%d�죬ץ�������������ȡ���°빦����Ч��\n",q);
	}
	else if(q==14)
	{
		printf("�������������ɵ��ٽ���\n");
	}
	else if(q>14)
	{
		printf("�������������ɵĵͳ��ڣ��˽׶α��⴦��һЩ��������\n");
	}
	//������������ 
	if(z==0)
	{
	    printf("�������������ɵ������գ��ʵ����������\n");
	}
	else if(z>0&&z<17)
	{
		printf("�������������ɵĸ߳��ڵĵ�%d�죬���������ʱ���ǿ��ѧϰ�����������İ���\n",z);
	} 
	else if(z==17)
	{
		printf("�������������ɵ��ٽ���\n");
	}
	else if(z>17)
	{ 
	printf("�������������ɵĵͳ���,�������ڴ��ڼ���һЩ���������Ļ\n");
	}
	}
	else
		printf("�����������Ͻǵ��˳�����\n");
	
	system("pause");
}
