# 2fa
This is a human contributed project detailing a list of websites and software 
supporting two factor authentication.

See the `sites/` directory for examples of configuration. The format of these 
files is described below. To add a new site, send a PR with your amend in the 
`sites/` directory and I'll get it merged.

This will shortly be automatically build on every merge, but for now, it's a 
manual process while a few things are ironed out.



### Format of a 2fa.json file:

The Google example contains the following:

	{
		"name": "Google",
		"url": "google.com",
		"type": "website",
		"ssl": true,
		"sms": true,
		"google": true,
		"hardware": true
	}

A more in depth look at each key is below. The `name` and `type` keys are the 
only two which are required at the moment. Any keys which have the value 
'false' may be omitted. The keys the current list of valid keys are:

Key 		| Required	| Explanation
----------- | --------- | ----------------------------------------------
name    	| Yes		| The human readable name of the website/service
type		| Yes		| One of 'website' or 'software'
url  		| No 		| The base URL of the website
ssl  		| No 		| Does the website support SSL?
sms  		| No 		| Support for SMS based 2FA?
email  		| No 		| Support for email based 2FA?
google 		| No 		| Support for Google Authenticator 2FA?
authy 		| No 		| Support for Google Authenticator 2FA?
hardware  	| No 		| Support for hardware 2FA?



### Contribute

If you have any comments, ideas or questions then please open an issue or PR 
and we can discuss.



### License

This project is licensed under the MIT license.