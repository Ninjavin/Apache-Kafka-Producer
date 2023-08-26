# Apache Kafka Producer Application with Spring Boot

This repository contains a Spring Boot application that acts as a Kafka producer. It demonstrates how to send messages to a Kafka topic using Apache Kafka and Spring Boot. The application runs on port 9191.

## Prerequisites

Before running the Kafka producer application, you need to set up a Kafka cluster locally. Follow the steps below to start a Kafka cluster on a Windows setup:

### Setting Up Kafka Cluster Locally (Windows)

1. **Download and Extract Kafka**:
   - Download the latest version of Apache Kafka from the official website: https://kafka.apache.org/downloads
   - Extract the downloaded archive to a directory of your choice.

2. **Start ZooKeeper**:
   - Open a command prompt and navigate to the Kafka directory.
   - Run the following command to start ZooKeeper:

     ```sh
     bin\windows\zookeeper-server-start.bat config\zookeeper.properties
     ```

3. **Start Kafka Broker**:
   - In a new command prompt window, navigate to the Kafka directory.
   - Run the following command to start the Kafka broker:

     ```sh
     bin\windows\kafka-server-start.bat config\server.properties
     ```

4. **Create a Kafka Topic**:
   - Open another command prompt window and navigate to the Kafka directory.
   - Run the following command to create a topic named "test-topic":

     ```sh
     bin\windows\kafka-topics.bat --create --topic test-topic --bootstrap-server localhost:9092 --partitions 1 --replication-factor 1
     ```

   You now have a Kafka cluster running locally with a topic named "test-topic."

## Getting Started with Kafka Producer Application

Follow these steps to set up and run the Kafka producer application:

1. **Clone the Repository**: Clone this repository to your local machine using the following command:

   ```sh
   git clone https://github.com/your-username/kafka-producer-spring-boot.git
   ```

2. **Configure Kafka Properties**:
   - Open the `src/main/resources/application.yml` file.
   - Update the `spring.kafka.bootstrap-servers` property to match your Kafka broker's address (e.g., `localhost:9092`).

3. **Build and Run the Application**

4. **Send Messages**:
   - Once the application is running, open Postman and send messages using the URL `http://localhost:9191/producer-app/publish/{message}` to send messages.
