Installing Jenkins
To update Ubuntu with Jenkins source lists, type in the following commands:

$ sudo wget -q -O - http://pkg.jenkins-ci.org/debian/jenkins-ci.org.key | sudo apt-key add -

$ sudo sh -c 'echo deb http://pkg.jenkins-ci.org/debian binary/ > /etc/apt/sources.list.d/jenkins.list'

$ sudo apt-get update

$ sudo apt-get install jenkins

Then, visit your server using port 8080, e.g. http://jenkins.lookahead.io:8080, and you should see the Jenkins startup screen:
You installed Jenkins on a Debian-based or a Fedora-based distribution, you can use the following commands:

Jenkins commands

$ sudo service jenkins restart

$ sudo service jenkins stop

$ sudo service jenkins start

Unlock
$ sudo vi /var/lib/jenkins/config.xml
Turn security off and remove the <authorizationStrategy> node

<useSecurity>false</useSecurity>
