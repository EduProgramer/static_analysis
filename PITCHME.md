---?image=assets/image/jeremy-bishop.jpg

# Static Analysis Basics

@fa[arrows gp-tip](Press F to go Fullscreen)

---?image=assets/image/kyle-gregory-devaras.jpg

# Definition

- Static program analysis is the analysis of computer software
that is performed without actually executing programs
- Analysis performed on executing programs is known as dynamic analysis |
- In most cases the analysis is performed on some version of the source code |

---?image=assets/image/kyle-gregory-devaras.jpg

## Tools

- probably your compiler
- CppCheck and CppCheck-gui (GPL)
- SonarCube (LGPL)
- Coverity (commercial)

---?image=assets/image/kyle-gregory-devaras.jpg

## CppCheck GUI

![CppCheck](assets/image/cppcheck.png)

---?image=assets/image/john-reign-abarintos.jpg

## Broken Code

```c++
int main(int argc, char const* argv[])
{
    int x = 10;

    if(x = 145)
    {
        x = x;
    }
    x = x;

    short k[13];
    k[13] = 123;

    return 0;
}
```
---?image=assets/image/kyle-gregory-devaras.jpg
## CppCheck Command
- cppcheck --enable=all --inconclusive  --xml --xml-version=2 -v  main.cpp 2> result.xml
- cppcheck-htmlreport --source-encoding="iso8859-1" --title="my project name" --source-dir=. --report-dir=. --file=result.xml
- rm result.xml

---?image=assets/image/john-reign-abarintos.jpg

## SonarCube

- Scanner / Server architecture
- plugin based
- Official C++ plugin is comercial but other languages are for free
- but there is a community C++ plugin

---?image=assets/image/john-reign-abarintos.jpg
![CppCheck](assets/image/sonarqube1.png)

---?image=assets/image/kyle-gregory-devaras.jpg
![CppCheck](assets/image/sonarqube2.png)

---?image=assets/image/kyle-gregory-devaras.jpg

![CppCheck](assets/image/sonarqube3.png)

---?image=assets/image/kyle-gregory-devaras.jpg

![CppCheck](assets/image/sonarqube4.png)

---?image=assets/image/kyle-gregory-devaras.jpg

![CppCheck](assets/image/sonarqube5.png)

---?image=assets/image/kyle-gregory-devaras.jpg
## SonarCube

Live live live

---?image=assets/image/kyle-gregory-devaras.jpg
# Thanks
