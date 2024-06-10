# Fast I/O to avoid Time Limit Exceeded

## Python
```python
import sys
n = int(sys.stdin.readline())
sys.stdout.write(str(n))
```

For multiple numbers input or a list input, you can use map() function, 
```python
import sys
x, y = list(map(int, sys.stdin.readline().split()))
sys.stdout.write(str(x+y))
```

## C++

```c++
#include <bits/stdc++.h> 
using namespace std; 
  
int main() 
{ 
    // added the two lines below 
    ios_base::sync_with_stdio(false); 
    cin.tie(NULL);  

    int x, y;
    // input and output  
    cin >> x >> y;
    cout << '\n';  // Don't use endl
     
    return 0; 
} 
```
Or you can just use scanf() and printf() functions,
```c++
#include <bits/stdc++.h> 
using namespace std; 
  
int main() 
{ 
    int x, y;
    scanf("%d %d", &x, &y);
    printf("%d", x+y);
    return 0; 
} 
```

## Java
Use buffer reader instead of scanner,
```java
import java.io.*;
import java.util.*; 
public class Main { 
	public static void main(String[] args) throws IOException
	{ 
        // fast input using buffer reader
		BufferedReader br = new BufferedReader(new InputStreamReader(System.in)); 
        StringTokenizer st = new StringTokenizer(br.readLine()); 
        int x = Integer.parseInt(st.nextToken()); 
        int y = Integer.parseInt(st.nextToken()); 
        int count = 0; 
        System.out.println(x+y); 
	} 
}
```
Or you can just use buffer reader inside scanner to use it like scanner and also use a faster way to output.

```java
import java.io.*;
import java.util.*; 
public class Main { 
	public static void main(String[] args) throws IOException
	{ 
        // fast input using buffer reader inside scanner
		Scanner sc = new Scanner(new BufferedReader(new InputStreamReader(System.in))); 
        int x = sc.nextInt(); 
        int y = sc.nextInt();

        // fast output using PrintWriter
        PrintWriter out = new PrintWriter(new BufferedOutputStream(System.out), true);
        out.println(x+y); 
	} 
}
```
# Resources
## Books
### Beginner friendly books to get started with competitive programming
* <a href="https://drive.google.com/file/d/1glUqhcDvEtVlyO_aOAcbLhVJuRw-fItC/view?usp=sharing">Competitive Programming in Python 128 Algorithms to Develop your Coding Skills (Christoph Dürr, Jill-Jênn Vie) <b>(Python)</b></a>
* <a href="https://drive.google.com/file/d/1zbunQkfEEMnHJ6CBCFe3811q9YiY_xqP/view?usp=sharing">Guide to Competitive Programming Learning and Improving Algorithms Through Contests (Undergraduate Topics in Computer Science) (Antti Laaksonen) <b>(C++)</b></a> (Best one)
### Books with topic-wise practice problems from previous ICPC problems (with solutions)
* <a href="https://drive.google.com/file/d/1XguI17mnM-cUEnLwWt2tyLC9QDRRfxbc/view?usp=sharing">Data-Structure-Practice (Yonghui-Wu, Jiande-Wang)</a>
* <a href="https://drive.google.com/file/d/1dUllVh8Jsw8eGuJIE2awIi3DTR8EO6Gb/view?usp=sharing">Algorithm-design-practice (Yonghui-Wu, Jiande-Wang)</a>
* <a href="https://drive.google.com/file/d/1HKVf4Ci6iqaVcQq_OR-l4jkNElPzNQJj/view?usp=sharing">Programming Challenges (Steven S. Skiena, Miguel A. Revilla)</a>
### Other competitive programming books
* <a href="https://drive.google.com/file/d/1Li6bLWpwA9EXK9JG0z3eDrwwsibLSJ-O/view?usp=sharing">Competitive Programming 3 The New Lower Bound of Programming Contests (Steven Halim)</a>
* <a href="https://drive.google.com/file/d/18VxajPyxW5XtGCXHDLnMVnSecB_Au4IE/view?usp=sharing">Dawn of Programming Contest (Md. Mahbubul Hasan)</a>
* <a href="https://drive.google.com/file/d/1t_wIdff-eqT0mUdJxbZjOPVQ19mwLAcp/view?usp=sharing">Art-of-Programming-Contest (Ahmed-Shamsul-Arefin)</a>
## Blogs/Discussions
To be added
## Youtube Channels
To be added
## Github Repositories
To be added
