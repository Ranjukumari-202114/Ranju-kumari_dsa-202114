# Ranju-kumari_dsa-202114




// Write a program  to implement all the binary tree traversal methods usings classes.

 #include <iostream>
 using namespace std;
 

 class Node
 {
 public:
    int data;
    Node *left, *right;
    
    
    Node(int data)
    {
        this->data = data;
        left = right = NULL;
    }
 

    void Preorder( Node *node)
    {
      if (node == NULL)
          return;
 
       cout<<node->data<<" ";
       Preorder(node->left);
       Preorder(node->right);
    
    }

    void Inorder( Node *node)
     {
       if (node == NULL)
           return;
 
        Inorder(node->left);
        cout<<node->data<<" ";
        Inorder(node->right);
   
     }
    void Postorder(Node *node)
     {
       if (node == NULL)
           return;
 
   
       Postorder(node->left);
       Postorder(node->right);
       cout << node->data<<" ";
   
     } 
     
};



int main()
{
    Node *root = new Node(76);
    root->left = new Node(45);
    root->right = new Node(54);
    root->left->left = new Node(32);
    root->left->right = new Node(48);
 
    cout<<"\nPreorder traversal of binary tree is \n";
    (*root).Preorder(root);
 
    cout<<"\nInorder traversal of binary tree is \n";
    (*root). Inorder(root);
 
    cout<<"\nPostorder traversal of binary tree is \n";
    (*root). Postorder(root);
    
    cout<<endl;
 
    return 0;
}

