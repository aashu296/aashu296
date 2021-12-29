- 👋 Hi, I’m @aashu296
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
aashu296/aashu296 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
#include <iostream>
using namespace std;

int main() {
	// your code goes here
	return 0;
}
#include<iostream>
using namespace std;
int main() {
    Node *takeinput_better(){
    int data;
    cin>>data;
    Node *head=NULL;
    NOde *tail = NULL;
    while(data!-1) {
        Node *newNode = new Node(data);
        if(head == NULL) {
            head = newNode ;
            tail = newNode;
            
        }
        else {
            tail -> next = newNode ;
            tail = tail->next;
            
        }
    }
    cin>>data;
    
} 
return head;
}]









Node* delete_Node(Node *head,int i){
    if(head == i ) {
        delete head;
        return NULL;
    }
    else {
        NOde *temp = head;
        int cnt=0;
        if(i==0) {
            delete head;
            head = head->next;
            return head;
        }
        while(cnt <i-1 && temp!=NULL ){
            temp = temp->next;
            cnt++;
        }
          temp->next = temp -> next -> next;
          delete temp->next;
          return head;
    }
    
    10 -> 20 -> 30-> 40-> 50-> NULL
    i=4
    cnt =0  max_cnt = 2
    100 -> 120  && cnt =0
    120 -> 140 && cnt =1
    140 -> 160  && cnt =2
    
    
  Node* insertion_rec(Node *head, int i, int data) {
      if(head == NULL) {
          return ;
      }
      if(i==0) {
          Node *newNode = new Node(data);
           newNode = head;
          return newNode;
      }
      Node *x = insertion_rec(head->next,i-1,data);
      head -> next =x;
      return head;
  }    
  
  Node* delete_rec(Node *head, int i) {
      if(head == NULL) {
          return;
      }
      if(i==0) {
          Node *temp =head->next;
          delete head;
          return temp;
      }
      Node *x =delete_rec(head->next, i-1);
      head -> next =x;
      return head;
  }
    
    
    
    
    int mid_Point(Node *head) {
        Node *slow = head;
        Node *fast = head->next;
        while(fast!=NULL || fast->next!=NULL) {
            fast = fast->next->next;
            slow = slow -> next;
        }
        int x = slow->data;
        return x;
    }
    
    Node* merge_list(Node *head1, Node *head2){
        Node *ft = NULL;
        Node *fh = NULL;
        while(fh!=NULL || ft !=NULL) {
            if(head1->data > head2->data){
                if(ft==NULL && fh==NULL){
                ft = head2;
                fh = head2;
                }
                else {
                 ft=head2;   
                }
                head2 = head2->next;
            }
            else {
                if(ft==NULL && fh == NULL){
                ft = head1;
                fh = head1;
                }
                else{
                    ft =head1;
                }
                head1 = head1->next;
            }
        }
        
           ft->next =(head1==NULL)?head2:head1; 
           return fh;
    }
    
  Node* merge_sort(Node*head) {
      if(mid==head||mid==temp){
          return;
      }
        Node *temp = Node *mid_point(head)->next;
        *mid_point(head)->next =NULL;
       Node *half1 = merge_sort(head); 
       Node *half2 = merge_sort(temp);
       return merge_list(half1,half2);
       
       
  }
  
    
