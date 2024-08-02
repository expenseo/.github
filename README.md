## **Project Overview**

Expenseo leverages modern cloud technologies to deliver a seamless experience in managing personal finances. The app listens for incoming bank email notifications, processes the transaction details, and updates the user's financial data in real-time.

## **Key Features**

### **Automated Transaction Updates**
Expenseo listens for incoming Gmail notifications related to bank transactions. Using AWS Lambda, the app processes these emails and extracts transaction details, which are then stored in Amazon DynamoDB.

### **GraphQL API**
A flexible and efficient GraphQL API, powered by AWS AppSync, allows users to manage transactions and query their financial data easily.

### **iOS Application**
A native iOS app built with SwiftUI displays the user's transaction data in an intuitive and visually appealing interface. Users can view, update, and manage their transactions effortlessly.

## **Technical Stack**

### **Backend**
- **Gmail API**: For reading and receiving notifications about bank transactions.
- **Google Pub/Sub**: To forward Gmail notifications.
- **AWS API Gateway**: To receive Pub/Sub notifications.
- **AWS Lambda**: For processing email transaction details.
- **AWS AppSync**: GraphQL API for querying and managing transaction data.
- **TypeScript**: Backend language for Lambda functions.

### **Database**
- **Amazon DynamoDB**: Scalable and reliable database for storing transactions and user data.

### **Frontend**
- **SwiftUI**: Native iOS UI framework for building the app interface.
- **Apollo Client for Swift**: Integration for GraphQL API.

## **Project Structure**

### **Backend Components**
1. **Gmail API**: Configured to read and push notifications for new emails.
2. **Google Pub/Sub**: Forwards notifications to AWS.
3. **AWS API Gateway**: Receives Pub/Sub notifications.
4. **AWS Lambda**: Processes email notifications, extracts transaction details, and updates DynamoDB.
5. **Amazon DynamoDB**: Stores transaction details.
6. **AWS AppSync**: Provides a GraphQL API for querying and managing transaction data.

### **Frontend Components**
1. **iOS Application**: Built using SwiftUI, provides an intuitive user interface for viewing and managing transactions.
2. **Apollo Client for Swift**: Connects the iOS app to the GraphQL API for seamless data interaction.
