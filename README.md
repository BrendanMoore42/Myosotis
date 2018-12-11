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
- Create virtual environment and `pip install twilio` or install/setup in directory from <a href="https://github.com/twilio/twilio-python">Twilio Github</a>

- Grab files from Myosotis
    <br>`$ git clone https://github.com/BrendanMoore42/Myosotis.git`
    
- Run user.py to set up friends.json and create events

### Shortcut Examples:
- Add friend without GUI:
    <br>```$ python add_friend.py Hermes 1507```
- Remove friend without GUI:
    <br>```$ python remove_friend.py Hermes```

### GUI Example:   
```
$ python user.py
========================= 

Welcome to Myosotis
Never forget a birthday again!

========================= 

Options: 
	1. Check Friend List
	2. Add Friend
	3. Remove Friend
	4. Test Phone
	5. Press "q" anytime to quit

Please choose an option: 
1 

Friends List:
Farnsworth 09/04
Fry 01/01
Leela 29/07 
Bender 04/09 
Zapp 30/06

========================= 

Options: 
	1. Check Friend List
	2. Add Friend
	3. Remove Friend
	4. Test Phone
	5. Press "q" anytime to quit
    
Please choose an option: 
2.

*Hint* Date format => Day/Month: ex. 28/07 

Please type name: 
Zoidberg
Please type date: 
05/05
Zoidberg added

=========================
```

3. Deploy
- Set cron job on local or real server through online cloud provider: AWS, Digital Ocean, etc.
- Example cron job for every day at noon:
    <br>`0 12 * * * /usr/bin/python3 /root/check_send.py >/dev/null 2>&1`

Always run the cron from the same directory as the friends.json
for up-to-date tasking.

<p align="center">
  <img src="https://img.crocdn.co.uk/images/products2/pl/20/00/01/88/pl2000018820.jpg?width=940&height=940" />
</p>
