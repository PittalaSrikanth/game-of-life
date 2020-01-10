node('UBUNTU')
{
stage('git-hub')
{
git 'https://github.com/PittalaSrikanth/game-of-life.git'
}
stage('maven-package')
{
sh label: '', script: 'mvn clean package'
}
stage('archive')
{
archive 'gameoflife-build/target/*.jar'
}
stage('maven')
{
sh label: '', script: 'echo build id $BUILD_ID branch name $GIT_BRANCH'
}
}
