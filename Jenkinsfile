pipeline {
agent any
stages {
stage('Clone') {
steps {
git 'https://github.com/abiya1999/Spetnaz.git'
}
}
stage('Build') {
steps {
sh 'mvn -e clean package' // For Java: mvn clean package
}
}
stage('Test') {
steps {
sh 'pytest tests/' // For Python
}
}
stage('Security Scan') {
steps {
sh 'dependency-check --scan ./ --out report'
}
}
}
}
