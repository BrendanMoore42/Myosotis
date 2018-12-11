# Myosotis
Inspired by the Forget-me-not flower this script uses Twilio's trail account service to send yourself reminders of important events, such as birthdays, anniversaries, etc. It's easy to miss emails but texts are certain to catch your eye. Go to <a href="https://www.twilio.com/try-twilio">Twilio</a> and sign up for a free trial. Verify your number through twilio to send free texts to yourself. 

## Requirements:
- Twilio==>v.6.2.1
- Twilio trial account (or paid number, if member)
- Python 3+

## Set-up
### Twilio
1. Log in to account and access console. In credentials.py, replace 'account' with Account SID and token with Auth Token. 
2. Get <a href="https://www.twilio.com/console/phone-numbers/incoming">phone number</a> and copy to credentials.py with '+' and country code. Add personal number to file. 

### Myosotis:
1. In bash, go to target directory on local machine or server to copy files:
    <br>`$ git clone https://github.com/BrendanMoore42/Myosotis.git`
    
2. Create database, add friends, set up information:
    <br>```$ python user.py```
    
3. Deploy
- Set cron job on local or real server through online cloud provider: AWS, Digital Ocean, etc.
- Example cron job for every day at noon:
    <br>`0 12 * * * /usr/bin/python3 /root/check_send.py >/dev/null 2>&1`

Always run the cron from the same directory as the friends.json
for up-to-date tasking.

<p align="center">
  <img src="https://img.crocdn.co.uk/images/products2/pl/20/00/01/88/pl2000018820.jpg?width=940&height=940" />
</p>
