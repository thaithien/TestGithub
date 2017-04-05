

# Maven Notes

## How to run Java main from Maven?

First We need to compile sources:
>`mvn compile`

Without arguments: 
>`mvn exec:java -Dexec.mainClass="com.vineetmanohar.module.Main"`

With arguments: 
>`mvn exec:java -Dexec.mainClass="com.vineetmanohar.module.Main" -Dexec.args="arg0 arg1 arg2"`






Credit: [3 ways to run Java from maven - vineetmanohar](http://www.vineetmanohar.com/2009/11/3-ways-to-run-java-main-from-maven/)

