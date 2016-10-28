# Postfix on CentOs


## mail log 如下
---
>
>        Oct 25 14:05:27 mail MailScanner[40478]: Commercial scanner clamav timed out!
>        Oct 25 14:05:27 mail MailScanner[40478]: clamav: Failed to complete, timed out
>        Oct 25 14:05:27 mail MailScanner[40478]: Virus Scanning: Denial Of Service attack is in message 33AC31294B1.A07EE

所有的信件都不能傳送或接收.

原因:

clamav 版本太舊, 更新後就解決這個問題





