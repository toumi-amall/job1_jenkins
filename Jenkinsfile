pipeline {
agent any
options {timestamps()}
stages {
stage('Cloner le dépôt'){
steps {
git url: 'https://github.com/toumi-amall/job1_jenkins.git', branch: 'master'
}
}
stage('Checkout'){
steps {
bat 'echo === Étape 1 : Vérification du dépôt ==='
bat 'git status'
}
}
stage('Build') {
steps {
bat 'echo === Étape 2 : Afficher le contenu du projet ==='
bat 'dir'
}
}
stage('Test') {
steps {
bat 'echo === Étape 3 : Simuler un déploiement local ==='
bat 'echo Le fichier index.html est prêt à être affiché'
}
}
stage('Deploy'){
steps {
bat 'echo === Étape 4 : Fin du build ==='
bat 'echo SUCCESS'
}
}
}
post {
success { echo ' Build OK'}
failure { echo ' Build KO' }
 }
}
