# 202001258_Lab5

### Tool used:
I have used pylint as a tool to perform static analysis

` pip install pylint `

### Github Repository:
The github repository I have used is 
https://github.com/kubernetes-client/python

### Execution:
` py -m pylint/setup.py `

![image](https://user-images.githubusercontent.com/83827570/227481905-b24ade09-e142-461e-8204-782144c8fcaa.png)

### Output:
![image](https://user-images.githubusercontent.com/83827570/227482059-7952afde-17ac-4526-b6e1-f24fea95b358.png)

### Understanding and resolving error

- Code error 1:

![image](https://user-images.githubusercontent.com/83827570/227483854-426216cc-2433-446a-86af-0401f67e3a20.png)

This can be resolved by ` "--disable=C0111" ` to ` "python.linting.pylintArgs": [], ` which was in the User's JSON settings.

- Code error 2:

![image](https://user-images.githubusercontent.com/83827570/227484284-c0d44f08-fa0a-4125-88e3-20806a182050.png)

It is better to specify an encoding when opening documents. Using the system default implicitly can create problems on other operating systems.

- Code error 3:

![image](https://user-images.githubusercontent.com/83827570/227484942-2fe5f292-5ca9-430a-a4a8-0d121bc7a332.png)

Used when we detect a string that is being formatted with format() or % which could potentially be a f-string. The use of f-strings is preferred. Requires Python 3.6 and ``py-version >= 3.6``.

- Other errors can be resolved in the same manner

It also suggest the rating of the code analysed.

![image](https://user-images.githubusercontent.com/83827570/227482456-af62b353-d4ab-4ac2-b91a-a180e05e5f2c.png)
