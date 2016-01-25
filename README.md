![Apache NiFi logo](http://nifi.apache.org/images/niFi-logo-horizontal.png "Apache NiFi")
# Getting Started with Apache NiFi Development


## Development Environment
Creating custom components in NiFi requires only two dependencies, Java JDK and Maven.  We will additionally require Git to make use of a sample repository.

### Java SDK (requires version 7+)

#### Do I need it?
* Execute `javac -version`.  If an error message about the command not being found or the response shows `javac 1.X.Y_ZZ` has X being less than 7, then JDK version 7 or later must be installed. 

#### Install
* Available for download via: [http://www.oracle.com/technetwork/java/javase/overview/index.html](http://www.oracle.com/technetwork/java/javase/overview/index.html)
 * _Linux_: OpenJDK versions 7+ are also supported and available 

### Maven (requires version 3.1.0+)

#### Do I need it?
* Execute `mvn -version`.  If an error message about the command not being found or the response shows `Apache Maven 3.X.Y` has X being less than 1, then Maven 3.1.0 or later must be installed.
 
#### Install
* Available via [http://maven.apache.org/download.cgi](http://maven.apache.org/download.cgi)
* Also available via homebrew for OS X and various Linux package management systems 

### Git

#### Do I need it?
* Execute `git --version`.  If an error message about the command not being found then git must be installed.

#### _Windows_
* **Executable client**:  [https://git-scm.com/download/linux](https://git-scm.com/download/linux) 
	
#### _OS X_
* A version is bundled with the Mac by default
* Newer version is available via the homebrew ecosystem: [http://brew.sh/](http://brew.sh/)
	
#### _Linux_
* **Aptitude based systems (Debian, Ubuntu)**:  `apt-get install git`
* **Yum based systems (RHEL, CentOS, Fedora)**:  `yum install git`
* **Other distributions**:  [https://git-scm.com/download/linux](https://git-scm.com/download/linux)


## Developing a Custom Processor Bundle Repository
* Check out the sample repository
`git clone https://github.com/apiri/nifi-sample-processor-bundle.git`


## Developing Custom Extensions from Archetype
We only need the repository checked out above, but in the case someone wishes to start from nothing, it is possible to generate the project structure above leveraging Maven Archetypes. 

### Making use of the [Apache NiFi Maven Archetypes](https://cwiki.apache.org/confluence/display/NIFI/Maven+Projects+for+Extensions)
* **[Processor Bundles](https://cwiki.apache.org/confluence/display/NIFI/Maven+Projects+for+Extensions#MavenProjectsforExtensions-MavenProcessorArchetype)**

Create using

```
mvn archetype:generate
	-DarchetypeGroupId=org.apache.nifi  
	-DarchetypeArtifactId=nifi-processor-bundle-archetype  
	-DarchetypeVersion=<NiFi Version>   
	-DnifiVersion=<NiFi Version>
```

* **[Controller Service Bundles](https://cwiki.apache.org/confluence/display/NIFI/Maven+Projects+for+Extensions#MavenProjectsforExtensions-ControllerServiceProjects)**

Create using

```
mvn archetype:generate
	-DarchetypeGroupId=org.apache.nifi  
	-DarchetypeArtifactId=nifi-service-bundle-archetype  
	-DarchetypeVersion=<NiFi Version>   
	-DnifiVersion=<NiFi Version>
```
