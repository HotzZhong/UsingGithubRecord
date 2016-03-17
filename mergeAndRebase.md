#UsingGithub
----
##分支 branch
####一、合并分支 merge branch
解决问题：为了测试的版本最终使用于默认版本
于是需要合并分支 
**Note：**合并后commit 将会影响主版本和分支版本（因为合并后NewCommit两个指针指向合并前两版本。）

![Alt text](./1458195851664.png)

----
####二、变基分支 rebase branch
解决问题：多个**工作流**，将**不同人对同个内容的修改**进行处理。
若无冲突将对两个修改都保留。

 
**冲突：**
![Alt text](./1458196635647.png)
**冲突后同步代码级提示：**
![Alt text](./1458196695064.png)

####对比：

	      D---E test  
	     /  
     A---B---C---F master     
使用merge合并：

	     D--------E  
	    /          \  
	A---B---C---F----G  test,master 
而使用rebase则：

	A---B---D---E---C'---F' test, master