# queue

### Constructor
``` C++
// constructing queues
#include <iostream>       // std::cout
#include <deque>          // std::deque
#include <list>           // std::list
#include <queue>          // std::queue

int main ()
{
  std::deque<int> mydeck (3,100);        // deque with 3 elements
  std::list<int> mylist (2,200);         // list with 2 elements

  std::queue<int> first;                 // empty queue
  std::queue<int> second (mydeck);       // queue initialized to copy of deque

  std::queue<int,std::list<int> > third; // empty queue with list as underlying container
  std::queue<int,std::list<int> > fourth (mylist);

  std::cout << "size of first: " << first.size() << '\n';
  std::cout << "size of second: " << second.size() << '\n';
  std::cout << "size of third: " << third.size() << '\n';
  std::cout << "size of fourth: " << fourth.size() << '\n';

  return 0;
}
```
Output:
> size of first: 0 <br>
> size of second: 3 <br>
> size of third: 0 <br>
> size of fourth: 2 <br>

### Member functions
``` C++
q.front() = 10;
q.back() = 10;
q.push(10);
q.pop(); // return void
```
