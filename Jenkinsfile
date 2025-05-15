// global variables 
// used across steps and stages. 
// persistant
// used in the groovy script

pipeline{
    agent any

    environment {
        // Used for shell variables ie. passing to sh. exits whilst pipeline runs 
        // creds/paths + in builts 
    }

    options{
        //timestamp() global
        //disableConcurrentBuilds() global
        //timeout (time: 10, unit: "minutes") global/local
        //retry(5) stage 
    }

    stages{
        stage("Make a directory"){
            options{timeout(time: 1, unit: 'MINUTES')}
            steps{
                //catchError (buildResult: 'UNSTABLE' , stageResult: 'USNTABLE'){
                //dir [jenkins-dir]
                sh "mkdir ~/jenkins-dir || true" // unique shell command- no scripting here!!
                //sh "cd jenkins-dir && touch file1.txt"
                //sh "touch file1.txt"
            }
            post{
                success{
                    echo "this was successful"
                }
                failure{
                    echo "failed"
                }
                always{
                    echo "this always prints"
                }
            }
        }

    
    }


}
