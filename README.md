#include<iostream>
using namespace std;
class node{
    public:                        
    int data;
    node* next ;                   // node type pointer 
    node(int data){
        this->data=data;
        this->next=NULL;
    }
    

};

void insertAtHead(node* &head,int d){
    node* temp =new node(d);         // when any data come new node has to create,here data =d
    temp->next=head;                 // temp ka next head ko point krega
    head=temp;                       //head ko hatake temp pe point kra do

}
// void insertAtTail(node* &tail,int d){
//     node* temp=new node(d);
//     tail->next=temp;
//     tail=tail->next; 
    
// }

// void insertAtPosition(node* &head,int position,int d){
//     node* temp=head;
//     int cnt=1;
//     while(cnt<position){
//         temp=temp->next;
//         cnt++;
//     }
//     node* nodeToInsert=new node(d);
//     nodeToInsert->next=temp->next;
//     temp->next>nodeToInsert;

    

// } 
void print(node* &head){
    node* temp=head;     // temp head ko point krega
    while(temp!=NULL){
        cout<<temp->data<<" ";
        temp=temp->next;         // temp pe next node ki address store hogi
    }
    
}
int main() 
{ 
    // node* node1=new node(10);
    // cout<<node1->data<<" ";
    // // cout<<node1->next<<endl; 
    // node* node2=new node(11); 
    // cout<<node2->data<<" ";

// ***************************For insertion at head(front)***************
    node* node1=new node(12);
    node* head=node1;                  // head pointed to node1
    print(head);
    insertAtHead(head,20);
    print(head);
    insertAtHead(head,23);
    print(head);

// // *****************For insertion at tail(end) ******************************

//     // node* node1=new node(10);
//     // node* tail=node1;
//     // print(tail);
//     // insertAtTail(tail,12);
//     // print(tail);
//     // insertAtTail(tail,15);
//     // print(tail);
    

// //************************  For insertion at middle***************



    

    return 0;
}






// ===========================================Circular linled list============================================


// #include<iostream>
// using namespace std;
// int main()
// {
//     class node{                           // class is used to create node
//         public:
//         int data;                        // a node contain data & next node pointer 
//         node* next;                      // node star type ka next ka pointer 

//         node(int d){                 // constructor to take input in node data & pointer 
//                 this->data =d;       // current object ka data or es node k data me d store hoga
//                 this->next=NULL;     // es nose k next me NULL store hoga as there is no any node next to curent node 
//          }

//     ~node(){
//         int value =this->data;
//         if(this->next!=NULL){
//             delete  next;
//             next =NULL;
//         }
//         cout<<"Memory is free for node with data"<<value<<endl;
//     }

//     };
//   void insertNode(node* &tail,int element,int d){      // after or before "int element " node have to insert & d is value in that node
      
//    // Assuming that the elemnet present in the list

//    if(tail==NULL){                                   // empty list
//       node* newNode=new node(d);                   // new node creation
//     tail=newNode;
//     newNode->next=newNode;m

//    }
//   }
   



//     return 0;
// }
