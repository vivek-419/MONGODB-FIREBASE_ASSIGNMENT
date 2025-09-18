Payment Security Survey & Real-Time Fraud Detection System
Team: Yash, Pratima, Armaan, Vivek

Tech: Node.js + Express + MongoDB + Chart.js

Features:
- User survey (demographics, payment methods, security fears)
- Real-time transaction simulation (10 dummy users)
- 9 fraud detection rules with risk scoring (0-99)
- Live fraud monitoring dashboard
- MongoDB Compass integration

Setup:
1. npm install
2. mongod --replSet rs0 --dbpath /path/to/db --bind_ip 127.0.0.1
3. mongosh -> rs.initiate({ _id: 'rs0', members: [{ _id: 0, host: '127.0.0.1:27017' }] })
4. npm run seed:users
5. npm run dev

Access:
- Dashboard: http://localhost:3000
- Survey: http://localhost:3000/survey.html
- Fraud Analysis: http://localhost:3000/fraud-analysis.html

MongoDB Compass: mongodb://127.0.0.1:27017/?replicaSet=rs0
Database: armaan_gang
Collections: users, transactions, fraud_logs, survey_responses

Fraud Rules: High amount outliers, rapid transactions, device/IP mismatch, odd hours, cross-user devices, impossible travel, velocity spending, money laundering patterns, account takeover risks.

