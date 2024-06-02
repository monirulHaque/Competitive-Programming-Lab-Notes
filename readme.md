# Fast I/O to avoid Time Limit Exceeded

## Python
```python
import sys
n = sys.stdin.readline()
sys.stdout.write(n)
```

For multiple numbers input or a list input, you can use map() function, 
```python
import sys
x, y = list(map(int, sys.stdin.readline()))
sys.stdout.write(x+y)
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
        out = new PrintWriter(new BufferedOutputStream(System.out), true);
        out.println(x+y); 
	} 
}
```