上传代码到GitHub：

0.git init (第一次执行即可)
1.git add -A
2.git commit -m "v1, can be compiled, not been tested on board"
3.git tag v1
4.git remote add origin https://github.com/hujinfan/APP_0003_Binder_C_App.git （第一次执行即可）
5.git push -u origin master
6.git push origin --tags

mount -t nfs -o nolock 192.168.7.163:/work /mnt

版本2：
运行service_manager报错：# binder: driver version differs from user space
错误原因：Makefile中arm-linux-gcc -DBINDER_IPC_32BIT=1 -I include -c -o $@ $<  
          写成了-BINDER_IPC_32BIT=1
1.git add -A
2.git commit -m "v2, modify run error"
3.git tag v2
4.git push origin master
5.git push origin --tags