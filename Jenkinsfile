pipeline { 
agent any 
stages { 
stage('Build') { 
steps { 
sh 'docker build -t myapp .' 
} 
} 
stage('Run Tests') { 
steps { 
sh 'docker run myapp mvn test' 
} 
} 
stage('Deploy') { 
steps { 
sh 'docker run -d -p 8080:8080 myapp' 
} 
} 
} 
} 
