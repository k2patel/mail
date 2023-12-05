# ./mail
Simple mail program to replace mailx, since using local relay without authentication.

## Configfile
 * use `.mailrc.sample` as reference for your setup.

## Help
```
usage: mail [-h] [--frm FRM] [--to TO] [--subject SUBJECT] [--msg MSG]

Send plain text email

options:
  -h, --help            show this help message and exit
  --frm FRM, -f FRM     Define from address (sender)
  --to TO, -t TO        Define to address (receipient)
  --subject SUBJECT, -s SUBJECT
                        Define subject
  --msg MSG, -m MSG     Define message, user input should end with `Ctrd + d` or send it through pipe
```
## Sample Usage
`echo xyz | mail -s 'testing' -t xyz@yahoo.com`
```
mail -s 'testing' -t xyz@yahoo.com
adfaserw
asdfasdfasd
Ctrl + d
```

#./smtptest
This program is written to test SMTP sending over TLS, specially when Certificate was signed by local CA.

## Configfile
 * no configuration require, just update the inscript variables at top.

## Help
```
usage: smtptest [-h] [--hostname HOSTNAME] [--ca CA] [--message MESSAGE] [--sender SENDER] [--recipient RECIPIENT] [--subject SUBJECT]
                [--starttls]

Send an email via SMTP

options:
  -h, --help            show this help message and exit
  --hostname HOSTNAME, -H HOSTNAME
                        SMTP server hostname (e.g., smtp.example.com)
  --ca CA, -c CA        Path to the CA file (e.g., /path/to/ca.pem)
  --message MESSAGE, -m MESSAGE
                        Email message
  --sender SENDER, -s SENDER
                        Sender's email address
  --recipient RECIPIENT, -r RECIPIENT
                        Recipient's email address
  --subject SUBJECT, -S SUBJECT
                        Email subject
  --starttls, -t        Use STARTTLS
```