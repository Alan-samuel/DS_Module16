# Ex4(C) B-Tree
## DATE:09/04/2025
## AIM:
To write a C function to delete an element in a B Tree.
## Algorithm
1. Start 
2. Try to delete the item from the node using delValFromNode. If not found, print "Not 
present" and return. 
3. If the node's count is 0 after deletion, set tmp to the current node and update myNode to its 
first linker child. 
4. Free the tmp node. 
5. Update the global root to the new myNode. 
6. Return after deletion. 
7. End  

## Program:
```
Program to write a C function to delete an element in a B Tree
Developed by: Alan Samuel Vedanayagam
RegisterNumber: 212223040012
```
```
struct BTreeNode{
int item[MAX+1], count;
struct BTreeNode*linker[MAX+1];
};

struct BTreeNode*root;*/
voiddelete(int item, struct BTreeNode*myNode) { struct BTreeNode*tmp; if(!delValFromNode(item, myNode)){ printf("Not present\n");
return;
} else{
if(myNode->count ==0) { tmp = myNode;
myNode=myNode->linker[0]; free(tmp);
}
}
root=myNode; return;
}
```
## Output:
![image](https://github.com/user-attachments/assets/791af199-681a-4808-8fa4-374681ea2a69)



## Result:
Thus, the C function to delete an element in a B Tree is implemented successfully.
