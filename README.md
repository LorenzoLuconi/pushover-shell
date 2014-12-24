# Shell script for Pushover notification
Script for [Pushover](http://pushover.net) notification in shell

## Usage

```
pushover [ -t <title> -u <user_key> -a <app_token> -s <sound> ] [message]
```	
 
Flags: 

 * -t title: add a message title 
 * -u user_key: ovverride ``USER_KEY`` variable. This is mandatory if ``USER_KEY`` is empty
 * -a app_token: ovverride ``APP_TOKEN`` variable. This is mandatory if ``APP_TOKEN`` is empty
 * -s sound: specify the sound to use for your message (default sound: pushover)
 * -d: dryrun

The message is optional: if empty the value of ``DEFAULT_MESSAGE`` variable is sent (default: "Shell Message")
	

## Examples

```bash
pushover -u <user_key> -a <app_key> this is my message
```

If ``USER_KEY`` and ``APP_TOKEN`` variables are not empty you can omit "-u" and "-a" parameters:

```bash
pushover this is my message
```

You can send message with command standard output: 

```bash
echo "this is the output of my command" | pushover -t "Long command complete"
```
