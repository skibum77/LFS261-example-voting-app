pipeline {
    agent any 

    stages{
        stage("one"){
            steps{
                echo 'step 1'
                sleep 3
            }
        }
        stage("two"){
            steps{
                echo 'step 2'
                sleep 9
            }
        }
        stage("three"){
            when{
                branch 'master'
                changeset "**/worker/**"
            }
                steps{
                    echo 'step 3'
                    sleep 2
                }
        }
        stage("four"){
            steps{
                echo "step more"
            }
        }
        stage("five-"){
            steps{
                echo "step more"
                sleep 3
            }
        }
    } 

    post{
      always{
          echo 'This pipeline is completed.'
      }
    }
}