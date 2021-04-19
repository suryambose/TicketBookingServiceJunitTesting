pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
              /// bat "rmdir  /s /q TicketBookingServiceJunitTesting"
                bat "git clone https://github.com/suryambose/TicketBookingServiceJunitTesting.git"
            }
        }
        stage('Mvn clean and install') {
            steps {
              /// bat "rmdir  /s /q TicketBookingServiceJunitTesting"
                bat "mvn clean -f TicketBookingServiceJunitTesting"
                bat "mvn install -f TicketBookingServiceJunitTesting"
            }
        }
        stage('test') {
            steps {
                bat "mvn test -f TicketBookingServiceJunitTesting"
            }
        }
        stage('package') {
            steps {
                bat "mvn package -f TicketBookingServiceJunitTesting"
            }
        }
    }
}
