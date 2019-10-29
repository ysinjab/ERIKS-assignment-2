node {
   stage('Download Code') { 
      git 'https://github.com/beerkeeper/python-ip-script'
   }
   stage('Run python') {
       // We have to isolate either with docker container or virtualenv
        withPythonEnv('python') {
            sh 'pip install -r requirements.txt'
            sh 'python main.py'
        }
   }
}