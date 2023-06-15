# skripttwitter
Skript Twitter
Script for sending scheduled messages in Discord chats
The script can send scheduled messages (f.e. every hour, every day, etc.) or one-time messages using specified delays. You can use it to submit your crypto wallets for whitelists, schedule GM/GN for specific chats, and farm !work/!daily shit in grind-based projects.

Pros
Safe use of your Discord tokens with proxies and user agents
Randomisation of delays
Specific settings for each Discord account
Message randomisation (fe ['gm', 'GM MFERS', 'gm!', 'GM'])
Cons
One-threaded, synchronous code
Logics
User specifies accounts in the txt file
Script initializes accounts, in case of fail - saves data to the 'data/failed_accounts' folder
Script starts sending messages according to the delay, start on run and loop settings
If the loop is disabled - the account is deleted from the queue after sending the first message
First start
Install python
Download the repo
Run cmd, navigate to the project folder
Run the command pip install -r requirements.txt to install all required dependencies
Prepare data in the 'data/accounts.txt' file. 1 line = 1 account. Check the 'data/accounts_sample' file to see the correct format.
custom_name_for_logs: choose any name, for logging purposes
discord_token: discord token that can be obtained from the browser's Network tab
http_proxy: proxy in format http://username:password@host:port
useragent: any useragent
discord_chat_id: id of the specific chat
['message1', 'message2', 'message3'.....]: list of messages, in case there is only 1 message - define it in the list as well (f.e. ['single_message'])
min_delay_sec: min delay before sending the message in seconds
max_delay_sec: max delay before sending the message in seconds
start_on_the_run_True_or_False: set True if you wish the bot to send the first message without delays right after you run the script, and set False if you wish to use the delay before the first message
loop_True_or_False: set True if you wish to send messages in the loop, set False if you wish to send only 1 message
Run the bot using the python discord_bulk_msg_sender.py command
Failed accounts can be found in the 'data/failed_accounts' folder
