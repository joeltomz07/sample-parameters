pipeline{
  agent any
  parameter{
    choice(name:'VERSION',choices:['1.1.0','1.1.1','1.1.2'],description:'Version used')
    booleanParam(name:'execute',defaultValue:true,description:'please execute')
  }
    stages{
      stage('build'){
        steps{
           echo "building the application"
        }
      }
      stage('test'){
        when{
          expression{
            params.execute
          }
        }
        
        steps{
          echo "testing the application"
        }
      }
      stage('deploy'){
        steps{
          echo "deploying the application"
          echo "deploying version ${prams.VERSION}"
        }
      }
    }
  }

