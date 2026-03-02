# DSA-code
#include<stdio.h>
#include<stdlib.h>
struct node
{
int data;
struct node* prev;
struct node* next;
};
void traverse()
{
  struct node* curr = NULL;
  printf("Linked list:");
  while(curr!=NULL)
  {
    curr= curr-> next;
  }
  
  while(curr!=NULL)
  {
    printf("%d", curr->data);
    curr = curr -> prev;
  }
} 
int main()
{
struct node* head = malloc (sizeof (struct node));
head->data = 10 ;

struct node* n2 = malloc (sizeof (struct node)); 
n2 -> prev = head;
n2-> data= 20;

struct node* n3 = malloc (sizeof (struct node));
n3 -> prev = n2;
n3-> data= 30;

struct node* n4 = malloc (sizeof (struct node));
n4 -> prev = n3;
n4-> data= 40; 
n4->next = NULL;

head -> next = n2; 
n2 -> next = n3;
n3 -> next = n4;
}
