// pipeline {
//     agent {
//         label 'AGENT-1'
//     }
//     options{
//         timeout(time: 10, unit: 'seconds') 
//         disableConcurrentBuilds()
//         //retry(1)
//     }
//     parameters {
//         string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        
//         text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

//         booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

//         choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

//         password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
//     }
//     stages {
//         stage('Build') { 
//             steps {
//                 sh 'echo This is Build'
//             }
//         }
//         stage('Test') { 
//             steps {
//                 sh 'This is test'
//             }
//         }
//         stage('Deploy') { 
//             steps {
//                 sh 'This is deploy'
//                 error 'pipeline failed'
//             }
//         }
//     stage ('print params') {
//         steps{
    
//                 echo "Hello ${params.PERSON}"

//                 echo "Biography: ${params.BIOGRAPHY}"

//                 echo "Toggle: ${params.TOGGLE}"

//                 echo "Choice: ${params.CHOICE}"

//                 echo "Password: ${params.PASSWORD}"
//           }  
//     }
//     } 

// post {
//     always{
//         echo"This sections runs always"
//         deleteDir() 
//     }
//     success{
//         echo "This section runs when pipeline success"
//     }
//     failure{
//         echo "This section runs when pipline failure"
//     }
// }
// }


pipeline {
    agent {
        label 'AGENT-1'
    }
    stages {
        stage('Build') { 
            steps {
                sh "echo this is build"
            }
        }
        stage('Test') { 
            steps {
                sh "echo this is test"
            }
        }
        stage('Deploy') { 
            steps {
                sh "echo this is Deploy"
                //error 'pipeline success'
            }
        }
    }
}
post {
    always{
        echo"This sections runs always"
        deleteDir() 
    }
    success{
        echo "This section runs when pipeline success"
    }
    failure{
        echo "This section runs when pipline failure"
    }
}
