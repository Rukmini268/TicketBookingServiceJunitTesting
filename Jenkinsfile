pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
                sh "rm  -s -q TicketBookingServiceJunitTesting"
                sh "git clone https://github.com/kishancs2020/TicketBookingServiceJunitTesting.git"
                sh "mvn clean -f TicketBookingServiceJunitTesting"
            }
        }
        stage('Build') {
            steps {
                sh "mvn clean package -f TicketBookingServiceJunitTesting"
            }
        }
        stage('test') {
            steps {
                sh "mvn test -f TicketBookingServiceJunitTesting"
            }
        }
        stage('package') {
            steps {
                sh "mvn package -f TicketBookingServiceJunitTesting"
            }
        }
    }
}
