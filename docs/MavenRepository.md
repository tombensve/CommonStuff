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
                    <url>http://dl.bintray.com/tommy/maven</url>
                </repository>
            </repositories>
            <pluginRepositories>
                <pluginRepository>
                    <snapshots>
                        <enabled>false</enabled>
                    </snapshots>
                    <id>central</id>
                    <name>bintray-plugins</name>
                    <url>http://dl.bintray.com/tommy/maven</url>
                </pluginRepository>
            </pluginRepositories>
        </profile>
    </profiles>
    <activeProfiles>
       <activeProfile>bintray</activeProfile>
    </activeProfiles>

I'm using a new service from JFrog (Artifactory) that provides you with multiple types of repositories to publish software to, where maven is just one kind. It also provides manual downloads, and download statistics. It is as of 2014-01-10 still in beta, and multi module projects cannot be synced to maven central through the service yet, but this has real potential when they have ironed out the bugs. It is available at [bintray.com](http://www.bintray.com). 

The above setup is taken directly from bintray. I don't think you should worry about them using the id "central", but if you are, change the id.

To browse my repo just bring upp [http://dl.bintray.com/tommy/maven](http://dl.bintray.com/tommy/maven) in a browser.
