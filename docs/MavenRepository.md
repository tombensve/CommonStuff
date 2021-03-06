# Maven Repository (at bintray)

Most of my github opensource project can be downloaded by maven (and other tools using maven repositories) by
adding the following repository in your settings.xml:

    <profiles>
        <profile>
            <id>tombensve-ns</id>
            <repositories>
                <repository>
                    <snapshots>
                        <enabled>false</enabled>
                    </snapshots>
                    <id>central</id>
                    <name>bintray</name>
                    <url>https://download.natusoft.se/maven</url>
                </repository>
            </repositories>
            <pluginRepositories>
                <pluginRepository>
                    <snapshots>
                        <enabled>false</enabled>
                    </snapshots>
                    <id>central</id>
                    <name>bintray-plugins</name>
                    <url>https://download.natusoft.se/maven</url>
                </pluginRepository>
            </pluginRepositories>
        </profile>
    </profiles>
    <activeProfiles>
       <activeProfile>tombensve-ns</activeProfile>
    </activeProfiles>

Since Bintray is shutting down I for now make the binaries available from my web server. 

Maven central has changed in how to submit stuff there since I sent my letter to maven users mailing list, which sonatype did not respond to, but JFrog/Bintray did.
Things seems slighly (only slightly!) better now, and I might look into this when I feel I have the time required. Bintray was brilliant and I'm very sad to se them go. 
