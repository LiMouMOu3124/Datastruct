#include"stdio.h"
#include"malloc.h"
#define MAXSIZE 100
typedef int DataType ;//定义一个新的数据类型 

typedef struct{//定义结构体用来定义一个基本单位 
	DataType Data[MAXSIZE] ;
	int last;
}SeqList; 

//建立顺序表在内存中分配存储位置 
SeqList *creatList(){
	SeqList *L=NULL;
	L=(SeqList*)(malloc(sizeof(SeqList)));
	return L; 
} 

//清空顺序表中的值 
void initList(SeqList*L) {
	L=NULL;
	L->last = -1;
}

//在表中输入数据
SeqList *putList(SeqList*L){
	int i =0;
	int value; 
	while(value!=0)
	{
		printf("输入你要存储的第%d个数据,若你想结束请输入0\n",i+1);
		scanf("%d",&value);
		if(value!=0){
			L->Data[i]=value;
		    i++;
		}
		
	}
	L->last=i;
	return L ;
} 

//求表长
int lengthList(SeqList*L) {
	return L->last+1;
}

//按序号查数据
DataType getElem(SeqList *L,int i){
	return L->Data[i+1];
} 

//按值查数据 
int  locateElem(SeqList*L,int i){
	int k =0;
	while(1){
		if(L->Data[k]=i){
			break;
		}else{
			k++;
		}
		
	}
	return k;
}

//插入数据
void insertElem(SeqList *L,int i,DataType j){
	if(L->last==MAXSIZE-1){
		printf("overflow");
	} 
	if((i<1)||(i>L->last+2)){
		printf("error");
	}
	for(j=L->last;j>=i-1;j--){
		L->Data[j+1]=L->Data[j];
		L->Data[i-1]=j;
		L->last++;
	}
} 
//删除数据
void deleteElem(SeqList *L,int i){
	int j;
	if(L->last==MAXSIZE-1){
		printf("overflow");
	} 
	if((i<1)||(i>L->last+1)){
		printf("此元素不存在");
	}
	for(j=i;j<=L->last;j++){
		L->Data[j-1]=L->Data[j];
		L->last--;
	}
} 

//打印数据表
void printList(SeqList *L){
	int i =0;
	while(L->Data[i]){
		printf("第一个数据是：%d\n",L->Data[i]);
		i++;
	}
} 

void menu(SeqList *L) //打印程序图形页面 	{
{
	int i ;
	DataType k;
	int cmd;
	int end = 0;
	while(1){
		printf("\n\n\n\n\n\n\n");
  printf("**************************************************************");
  printf("\n顺序表操作\n");
  printf("1.清空顺序表中的值\n");
  printf("2.求表长\n");
  printf("3.按序号查数据\n");
  printf("4.按值查数据\n");
  printf("5.插入数据\n");
  printf("6.删除数据\n");
  printf("7.打印数据表\n");
  printf("0.退出\n");
  printf("**************************************************************");
  printf("\n\n\n\n\n\n\n");
  printf("输入你需要进行的操作: ");
  scanf("%d", &cmd);
  switch (cmd)
  {
  case 1:
   initList(L);
   break;
  case 2:
   lengthList(L);
   break;
  case 3:
   getElem(L,i);
   break;
  case 4:
   locateElem(L,i);
   break;
  case 5:
   insertElem(L, i, k);
   break;
  case 6:
   deleteElem(L,i);
   break; 
  case 7:
   printList(L);
   break;    
  case 0:
   end = 1;
   break;
  default:
   printf("错误输入!\n");
  }
  if (end == 1){
   break;
}
	}
}

void main(){
	SeqList *L; //建立顺序表 
	
	creatList(&L);//分配存储空间 
	
	putList(&L); //填入数据 
	
	menu(&L);    //打印菜单页 
}
