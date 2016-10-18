# msh
An easy to use shell menu, the view and function are seperated. The view is in msh.etc file, and the function is in msh.fun file. What's showing in the menu is easy to change by only editing the msh.etc file.
# Installing and Running
Get the code:
```
git clone https://github.com/qihaiyan/msh.git
```
Then run:
```
cd msh
```
```
sh msh.sh
```
or
```
chmod u+x msh.sh
./msh.sh
```

![msh](https://cloud.githubusercontent.com/assets/5896784/19466245/370baa86-953c-11e6-8049-f99c7a4bf4b4.jpeg)

# msh.etc
The definitation of the menu with msh.etc is very simple:
```
PROMPT	Input your choice
BANNER	banner	banner
1	mysubmenu	submenu	banner1
1-1	menufun1-1	fun101	1
1-2	menufun1-2	fun102	1	1-1
2 menufun2 fun2 1 1-1
```
There are 5 fields separated with TAB char in this file for the menu contect.

1. Menu Id
2. Menu Name
3. Function Name, if this menu has sub menus, the function name must be hard written to submenu
4. Required Flag, used to define if this menu is must to execute
5. Depend Menu Id, current menu can be to use only if the depended menu has been successfully executed

The fun101, fun102 ... is the funtion name we defined in msh.fun,
when we choose a menu id, the correspond function will be called.
# msh.fun
msh.fun is just a shell file, we can define funtions refered in msh.etc .
``` bash
banner(){
	echo "            TOP-MENU"
	echo "  ============================="
}
banner1(){
	echo "            SUB-MENU"
	echo "  ============================="
}
fun101(){
	echo "function 101 executed."
}
fun102(){
	date
}
fun2(){
  echo "function 2 executed."
  return 2
}
```
