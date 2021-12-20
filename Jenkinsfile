pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh "mvn -B TicketBookingServiceJunitTesting clean package"
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
