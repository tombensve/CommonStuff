# Maven Repository (at bintray)

Most of my github opensource project can be downloaded by maven (and other tools using maven repositories) by
adding the following repository in your settings.xml:

    <profiles>
        <profile>
            <id>bintray</id>
            <repositories>
                <repository>
                    <snapshots>
                        <enabled>false</enabled>
                    </snapshots>
                    <id>central</id>
                    <name>bintray</name>
                    <url>http://jcenter.bintray.com/</url>
                </repository>
            </repositories>
            <pluginRepositories>
                <pluginRepository>
                    <snapshots>
                        <enabled>false</enabled>
                    </snapshots>
                    <id>central</id>
                    <name>bintray-plugins</name>
                    <url>http://jcenter.bintray.com/</url>
                </pluginRepository>
            </pluginRepositories>
        </profile>
    </profiles>
    <activeProfiles>
       <activeProfile>bintray</activeProfile>
    </activeProfiles>

I'm using a new service from JFrog that provides you with multiple types of repositories to publish software to, where maven is just one kind. It also provides manual downloads, and download statistics. It is available at [bintray.com](http://www.bintray.com). 

Do note that the above jcenter repository is a superset of maven central!

To browse binaries & docs for any of my projects at bintray go to: https://bintray.com/tommy/maven/&lt;project&gt;/view 
