# Snippets
## File
### Append a file
```c++
#include <fstream>

std::ofstream file;
file.open("path", std::fstream::app);
file << "data\n";
file.close();
```

## Time
### Get a human readable timestamp
* pre C++ 11
  * [Time formats](http://en.cppreference.com/w/cpp/chrono/c/strftime)
```c++
#include <time.h>

time_t now = ::time(0);
struct tm  tstruct;
char buf[100];

tstruct = *localtime(&now);
strftime(buf, sizeof(buf), "%Y-%m-%d %X", &tstruct);
```

## Doxygen
```c++
/// doc

/*!
 * Send data
 * @param buffer a data
 * @return the number of bytes actually sent
 */
```
