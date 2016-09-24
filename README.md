Android-based Code Offload Converter
====================================
The tool explores the classes of an Android project and transforms the annotated methods (``` @Cloud ```) into offloadable components that can be processed remotely by a virtualized Dalvik machine in the cloud. How to deploy AOSP/CyanogenMod Dalvik in a x86 server can be found here [1](https://gist.github.com/huberflores/4687766), [2](https://gist.github.com/huberflores/4714824). We can also provide you with a ready-to-use Dalvik x86 in Amazon EC2. Please contact huber AT ut DOT ee for more information.


![alt text](https://raw.github.com/huberflores/CodeOffloadingAnnotations/master/UT_OffloadingModel.png "Offloading model")

[Figure's reference](http://www.sciencedirect.com/science/article/pii/S0164121213002318)


Requirements
-------------

Maven : version >= 3.0.4

JDK : version >= 1.7


Build
------------
Download the source and navigate into the root directory.

```xml
$ git clone https://github.com/huberflores/CodeOffloadingAnnotations.git
````

Build the project with Maven 

```xml
$ mvn clean install
````
Then move into the converter directory and run 

```xml
$ mvn org.apache.maven.plugins:maven-assembly-plugin:2.2-beta-2:assembly
````

Try Application 
------------
A file "converter-1.0-jar-with-dependencies" would be created in target folder of the converter directory.
Navigate into the directory via the command prompt and execute the following

```xml
$ java -jar converter-1.0-jar-with-dependencies.jar
````

[End-to-end example](https://github.com/huberflores/ComputationalOffloadingDemo.git)

More examples can be found [here](https://github.com/alirezaostovar/codeoffloading)

More detailed instructions [here](https://gist.github.com/huberflores/9168683)

How to cite
-----------
This tool is built for comparison purposes between our proposed approach and current code offloading mechanisms. If you are using the tool for your research, please do not forget to cite. Thanks!


- H. Flores, and S.N. Srirama. ["Adaptive code offloading for mobile cloud applications: Exploiting fuzzy sets and evidence-based learning."](http://dl.acm.org/citation.cfm?id=2482984) Proceeding of the fourth ACM workshop on Mobile cloud computing and services. ACM, 2013. In conjunction with, the 11th International Conference on Mobile Systems, Applications and Services (MobiSys 2013).


**BibTex**
```xml
@inproceedings{flores2013adaptive,
  title={Adaptive code offloading for mobile cloud applications: Exploiting fuzzy sets and evidence-based learning},
  author={Flores, Huber and Srirama, Satish},
  booktitle={Proceeding of the 4th ACM MobiSys workshop on Mobile cloud computing and services},
  pages={9--16},
  year={2013},
  organization={ACM}
}
``` 



