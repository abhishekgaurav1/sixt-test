node {
    stage ("git pull") {
        echo "downloding from git repo"
        
    }
    stage ("build") {
        echo "do your build step here"
    }
    stage ("approve for deployment") {
        input message: "Do you want to approve this job to deploy to production?", ok: "OK", submitter: "abhishek"
    }
    stage ("deploy to stage") {
        echo "deployiong"
    }
}
