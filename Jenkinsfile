node {
   stage('Download Code') { 
      git 'https://github.com/beerkeeper/python-ip-script'
   }
   stage('Run python') {
        withPythonEnv('python') {
            sh 'pip install -r requirements.txt'
            sh 'python main.py'
        }
   }
}