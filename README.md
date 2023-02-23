# mail
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
