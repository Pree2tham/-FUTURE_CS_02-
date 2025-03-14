                         Phishing simulation report 

 smtplib
from email.mime.text import MIMEText

def send_phishing_email(target_email, fake_sender):
    msg = MIMEText("Click this link: http://malicious.link")
    msg['Subject'] = "Urgent: Account Verification Required"
    msg['From'] = fake_sender
    msg['To'] = target_email

    with smtplib.SMTP('smtp.gmail.com', 587) as server:
        server.starttls()
        server.login("your-email@gmail.com", "app-password")
        server.sendmail(fake_sender, target_email, msg.as_string())

# WARNING: Only use with explicit consent and legal authorization.
