node {
    stage ("git pull") {
        git url: "https://github.com/abhishekgaurav1/javaee7-simple-sample.git", credentialsId: '4abb7509-fdc7-40ad-b664-478777cd1c3b'
     
    }
    stage ("build") {
        sh "mvn clean install"
        echo "do your build step here"
    }
    stage ("approve for deployment") {
        input message: "Do you want to approve this job to deploy to production?", ok: "OK", submitter: "abhishek"
    }
    stage ("deploy to stage") {
        sh "cp target/javaee7-simple-sample.war ~/apache-tomcat-8.5.31/webapps/test.war"
    }
}
