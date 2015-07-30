
## Create new projects
`cocos new MyNewGame -l js -d /Users/Documents/Game`

#Create a new project

##Create a Cocos2d-JS project:

`cocos new projectName -l js`
##Create a project contains web engine only:

`cocos new projectName -l js --no-native`
##Create a project in a specified directory:

`cocos new projectName -l js -d ./Projects`
##Run the project

###Run Cocos2d-JS project with a web server :
```
cd directory/to/project
cocos run -p web
```
###Publish your project on web with Closure Compiler's advanced mode :
```
cd directory/to/project
cocos compile -p web -m release --advanced
```
###Compile and run project on native platforms :
```
cd directory/to/project
cocos compile -p ios|mac|android|web
cocos run -p ios|mac|android
```

##Useful options
```
-p platform : The platform can be ios|mac|android|web.
-s source   : Your project directory, if not specified the current directory will be used.
-q          : Quiet mode, remove log messages.
-m mode     : Mode debug or release, debug is default
--source-map: General source-map file. (Web platform only)
--advanced  : Use Closure Compiler's advanced mode to compress JavaScript codes. (Web platform only)
```
##Help

And if you have any doubt about the usage, please use -h with any command to have some help messages. Here are all three commands:
```
new for creation
compile for compilation
run for execution
```
