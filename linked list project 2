#include <iostream> // hussien_mosalam project
using namespace std;
class node // making the node
{
public:
    int data;
    node *next;
    node()
    {
        data = 0;
        next = NULL;
    }
};
class linkedlist // the linked_list class
{
public:
    int length = 0;
    node *head, *last;
    linkedlist()
    {
        length = 0;
        head = NULL;
        last = NULL;
    }
    void empty_checker()
    {
        if (length == 0)
        {
            cout << "this list is empty" << endl;
            cout << "if you want to insert_first press 1 if you want to exit press 0" << endl;
            int x;
            int a;
            string b;
            double c;
            cin >> x;
            if (x == 1)
            {
                cout << "enter the node value" << endl;
                cin >> a;
                cout << endl;
                insert_first(a);
            }
        }
        else if (length != 0)
            return;
    }
    void insert_first(int element)
    {
        node *new_node = new node;
        new_node->data = element;
        if (length == 0)
        {
            head = last = new_node;
            new_node->next = NULL;
        }
        else if (length == 1)
        {
            cout << "this list has an element in it try using insert_begin()" << endl;
            return;
        }
        else
        {
            cout << "this list has elements in it try using insert_begin()" << endl;
            return;
        }
        length++;
    }
    void insert_begin(int element)
    {
        empty_checker();
        node *new_node = new node;
        new_node->data = element;
        if (length != 0)
        {
            new_node->next = head; // لانه اخد الهيد في اللي قبلهاو بالاسايمنت النكست اخذ قيمة العنوان بتاعة الهيد عشان يأكسس على البيانات بتعته
            head = new_node;
        }
        else
        {
            cout << "this list doesn't have a first element try using insert_first()" << endl;
            return;
        }
        length++;
    }
    void insert_last(int element)
    {
        node *new_node = new node;
        new_node->data = element;
        if (length != 0)
        {
            new_node->next = NULL;
            last->next = new_node;
            last = new_node;
        }
        else
        {
            cout << "this list has no elements" << endl;
            return;
        }
        length++;
    }
    void insert_pos(int pos, int element)
    {
        node *new_node = new node; // heap
        new_node->data = element;
        // declaration and initialization is done
        node *counter = head;
        for (size_t i = 0; i < pos; i++)
        {
            counter = counter->next; // هنا الكاونتر يساوي النود حرفيا وليس يؤشر عليه
        }
        new_node->next = counter->next;
        counter->next = new_node;
        length++;
    }
    void delete_pos(int pos)
    {
        node *ptr = head, *ptr2 = head;
        ptr2 = ptr2->next;
        if (length == 1)
        {
            /* code */
            delete head;
            length--;
        }
        else
        {
            for (size_t i = 0; i < pos - 1; i++)
            {
                /* code */
                ptr = ptr->next;
                ptr2 = ptr->next;
            }
            ptr = ptr2->next;
            delete ptr2;
            length--;
        }
    }
    void get_length()
    {
        cout << "the length of the list is : " << length << endl;
    }
    void print_list()
    {
        node *ptr = head;
        for (size_t i = 0; i < length; i++)
        {
            cout << ptr->data << endl;
            ptr = ptr->next;
        }
    }
};
int main()
{
    int a, b, c;
    linkedlist list;
    list.insert_first(1);
    list.insert_last(2);
    list.insert_last(3);
    list.delete_pos(2);
    list.get_length();
    list.print_list();
}
