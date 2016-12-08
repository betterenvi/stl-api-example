# deque

### Constructor

``` C++
// constructing deques
#include <iostream>
#include <deque>

int main ()
{
  unsigned int i;

  // constructors used in the same order as described above:
  std::deque<int> first;                                // empty deque of ints
  std::deque<int> second (4,100);                       // four ints with value 100
  std::deque<int> third (second.begin(),second.end());  // iterating through second
  std::deque<int> fourth (third);                       // a copy of third

  // the iterator constructor can be used to copy arrays:
  int myints[] = {16,2,77,29};
  std::deque<int> fifth (myints, myints + sizeof(myints) / sizeof(int) );

  std::cout << "The contents of fifth are:";
  for (std::deque<int>::iterator it = fifth.begin(); it!=fifth.end(); ++it)
    std::cout << ' ' << *it;

  std::cout << '\n';

  return 0;
}
```
Output:
> The contents of fifth are: 16 2 77 29 

### Element access
``` C++
dq[i] = 10;
dq.at(i) = 10;
dq.front() = 10;
dq.back() = 10;
```

### Modifiers
``` C++
dq.push_back(10);
dq.push_front(10);
dq.pop_back(); // return void
dq.pop_front(); // return void
```
