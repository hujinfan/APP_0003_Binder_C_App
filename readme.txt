�ϴ����뵽GitHub��

0.git init (��һ��ִ�м���)
1.git add -A
2.git commit -m "v1, can be compiled, not been tested on board"
3.git tag v1
4.git remote add origin https://github.com/hujinfan/APP_0003_Binder_C_App.git ����һ��ִ�м��ɣ�
5.git push -u origin master
6.git push origin --tags

mount -t nfs -o nolock 192.168.7.163:/work /mnt

�汾2��
����service_manager����# binder: driver version differs from user space
����ԭ��Makefile��arm-linux-gcc -DBINDER_IPC_32BIT=1 -I include -c -o $@ $<  
          д����-BINDER_IPC_32BIT=1
1.git add -A
2.git commit -m "v2, modify run error"
3.git tag v2
4.git push origin master
5.git push origin --tags

�������
# ./service_manager &
# ./test_server &
# ./test_client hello
# ./test_client hello hujinfan
# killall service_manager test_server

�汾3��
1.git add -A
2.git commit -m "v3, test and run"
3.git tag v3
4.git push origin master
5.git push origin --tags

�汾4��
1.git add -A
2.git commit -m "v4, add saygoodbye and saygoodbye_to"
3.git tag v3
4.git push origin master
5.git push origin --tags