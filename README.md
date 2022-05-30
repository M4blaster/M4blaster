- 👋 Hi, I’m @M4blaster
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
M4blaster/M4blaster is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
#include <iostream>
using namespace std;
typedef struct
{
 int wt;
 int bt;
 int tat;
 int priority;
 string name;
} process;
int main()
{
 int n;
 cout << "Enter num of process: ";
 cin >> n;
 process *p = new process[n];
 for (int i = 0; i < n; i++)
 {
 cout << "Enter process name and burst time : ";
 cin >> p[i].name >> p[i].bt;
 }
 p[0].wt = 0;
 p[0].tat = p[0].bt + p[0].wt;
 for (int i = 1; i < n; i++)
 {
 p[i].wt = p[i - 1].tat;
 p[i].tat = p[i].bt + p[i].wt;
 }
 int avgWT = 0;
 int avgTat = 0;
 cout << "Process Bt Wt Tat" << endl;
 for (int i = 0; i < n; i++)
 {
 cout << p[i].name << " : " << p[i].bt << " "
 << p[i].wt << " " << p[i].tat << endl;
 avgWT += p[i].wt;
avgTat += p[i].tat;
 }
 cout << "Average waiting time : " << avgWT / n << endl;
 cout << "Average turn around time : " << avgTat / n << endl;
 return 0;
}
