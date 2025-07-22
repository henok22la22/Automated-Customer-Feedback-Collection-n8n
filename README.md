# Automated-Customer-Feedback-Collection-n8n
This project automates the entire customer feedback collection process after a product is ordered and delivered. It is designed for e-commerce platforms like Shopify, WooCommerce, or custom websites using n8n as the core automation engine. 

Once a customer places an order, the system automatically stores the order details and sends a confirmation email thanking them. Then, after a short wait period (usually 2–3 days, or based on delivery status), the system checks daily whether the order has been delivered.

If the delivery is confirmed, the system sends a personalized feedback request via email. This email contains a survey link or embedded form where the customer can submit their thoughts about the product or service.

After the customer submits feedback, the system captures it via a form trigger, stores the feedback in a database, and optionally notifies internal teams (like customer support or product teams) to analyze and take action if needed.

# Flow Detail:
1.	Incoming Order (Webhook Trigger)
  o	Receives order data from Shopify, WooCommerce, or a custom site.
2.	Store Order Details
  o	Saves order info to a database.
3.	Send Confirmation Email
  o	Sends a "Thank you for your order" email.
4.	Daily Checking (Schedule Trigger)
  o	Checks daily if the order is delivered (after 2–3 days or using delivery status).
5.	Send Feedback Request
  o	After delivery, sends a survey/form link via email.
6.	Wait Customer Feedback (Form Submission Trigger)
  o	Waits until the customer submits feedback.
7.	Receive Feedback
  o	Captures submitted feedback and triggers internal analysis.
8.	Store with Settlement
  o	Stores feedback and optionally notifies the team or updates internal systems.

# Technologies/Tools Used:
•	n8n (automation)
•	Webhook (to receive orders)
•	Scheduler (daily delivery check)
•	Email nodes (confirmation and feedback emails)
•	Forms or Typeform (for collecting feedback)
•	Database or Google Sheets (for storing order and feedback data)
