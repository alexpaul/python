# Send email 

```python
import smtplib
from email.mime.text import MIMEText
from email.mime.multipart import MIMEMultipart

def send_email(recipient, subject, body):
    # Create message container
    msg = MIMEMultipart()
    msg['From'] = ""
    msg['To'] = recipient
    msg['Subject'] = subject

    # Add body to email
    msg.attach(MIMEText(body, 'plain', 'utf-8'))

    # Create SMTP connection
    s = smtplib.SMTP("smtp.gmail.com", 587)
    s.starttls()
    # App passwords are not recommended
    # See docs here: https://support.google.com/accounts/answer/185833?hl=en
    s.login("{ your gmail here }", "{ your gmail app password here }")
    
    # Convert message to string and send
    text = msg.as_string()
    s.sendmail("{ recipient's email }", recipient, text)
    s.quit()
    
    print("Sending email...")
    print(f"To: {recipient}")
    print(f"Subject: {subject}")
    print(f"Body: {body}")
    return "Sent!"
```
