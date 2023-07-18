# log job

```bash
+ rm -r jenkins-pipeline-test
+ git clone https://****:****@github.com/****/jenkins-pipeline-test.git
Cloning into 'jenkins-pipeline-test'...
+ cd jenkins-pipeline-test
+ date
+ echo Tue Jul 18 22:05:22 UTC 2023 - PRjob executed
+ cat job.log
Tue Jul 18 21:14:45 UTC 2023 - PRjob executed
Tue Jul 18 21:19:00 UTC 2023 - PRjob executed
Tue Jul 18 21:20:50 UTC 2023 - PRjob executed
Tue Jul 18 21:21:19 UTC 2023 - PRjob executed
Tue Jul 18 21:38:41 UTC 2023 - PRjob executed
Tue Jul 18 21:40:35 UTC 2023 - PRjob executed
Tue Jul 18 21:42:43 UTC 2023 - PRjob executed
Tue Jul 18 21:45:34 UTC 2023 - PRjob executed
Tue Jul 18 21:51:15 UTC 2023 - PRjob executed
Tue Jul 18 21:54:40 UTC 2023 - PRjob executed
Tue Jul 18 21:56:16 UTC 2023 - PRjob executed
Tue Jul 18 21:57:53 UTC 2023 - PRjob executed
Tue Jul 18 21:58:28 UTC 2023 - PRjob executed
Tue Jul 18 22:01:45 UTC 2023 - PRjob executed
Tue Jul 18 22:03:07 UTC 2023 - PRjob executed
Tue Jul 18 22:05:22 UTC 2023 - PRjob executed
+ git add .
+ git -c user.email=jenkins@jenkins.ru commit -m update log
[main 4dac514] update log
 1 file changed, 1 insertion(+)
+ git push
To https://github.com/****/jenkins-pipeline-test.git
   c80da48..4dac514  main -> main
```

# log email sending


```bash
REST API
Jenkins 2.401.2
Stage Logs (Declarative: Post Actions)
 Extended Email (self time 1s)
Sending mail from default account using custom from address pcserg@yandex.ru
messageContentType = text/plain; charset=UTF-8
Adding recipients from project recipient list
Analyzing: gurov@surf.dev
Looking for: gurov@surf.dev
	starting at: 0
	firstFoundIdx: 0
	firstFoundIdx-substring: gurov@surf.dev
	=> found type: 0
Analyzing: gurov@surf.dev
Looking for: gurov@surf.dev
	starting at: 0
	firstFoundIdx: 0
	firstFoundIdx-substring: gurov@surf.dev
	=> found type: 0
Analyzing: gurov@surf.dev
Looking for: gurov@surf.dev
	starting at: 0
	firstFoundIdx: 0
	firstFoundIdx-substring: gurov@surf.dev
	=> found type: 0
Adding recipients from trigger recipient list
Successfully created MimeMessage
Sending email to: gurov@surf.dev
DEBUG: getProvider() returning jakarta.mail.Provider[TRANSPORT,smtp,com.sun.mail.smtp.SMTPTransport,Oracle]
DEBUG SMTP: need username and password for authentication
DEBUG SMTP: protocolConnect returning false, host=smtp.yandex.ru, user=root, password=<null>
DEBUG SMTP: useEhlo true, useAuth true
DEBUG SMTP: trying to connect to host "smtp.yandex.ru", port 465, isSSL false
220 mail-nwsmtp-smtp-production-main-44.sas.yp-c.yandex.net (Want to use Yandex.Mail for your domain? Visit http://pdd.yandex.ru) 1689717923-N5p8495DYSw0
DEBUG SMTP: connected to host "smtp.yandex.ru", port: 465
EHLO 43be239ec0c2
250-mail-nwsmtp-smtp-production-main-44.sas.yp-c.yandex.net
250-8BITMIME
250-PIPELINING
250-SIZE 53477376
250-STARTTLS
250-AUTH LOGIN PLAIN XOAUTH2
250-DSN
250 ENHANCEDSTATUSCODES
DEBUG SMTP: Found extension "8BITMIME", arg ""
DEBUG SMTP: Found extension "PIPELINING", arg ""
DEBUG SMTP: Found extension "SIZE", arg "53477376"
DEBUG SMTP: Found extension "STARTTLS", arg ""
DEBUG SMTP: Found extension "AUTH", arg "LOGIN PLAIN XOAUTH2"
DEBUG SMTP: Found extension "DSN", arg ""
DEBUG SMTP: Found extension "ENHANCEDSTATUSCODES", arg ""
DEBUG SMTP: protocolConnect login, host=smtp.yandex.ru, user=pcserg@yandex.ru, password=<non-null>
DEBUG SMTP: Attempt to authenticate using mechanisms: LOGIN PLAIN DIGEST-MD5 NTLM XOAUTH2 
DEBUG SMTP: Using mechanism LOGIN
DEBUG SMTP: AUTH LOGIN command trace suppressed
DEBUG SMTP: AUTH LOGIN succeeded
DEBUG SMTP: use8bit false
MAIL FROM:<pcserg@yandex.ru>
250 2.1.0 <pcserg@yandex.ru> ok 1689717924-N5p8495DYSw0-YqriOY9b
DEBUG SMTP: sendPartial set
RCPT TO:<gurov@surf.dev>
250 2.1.5 <gurov@surf.dev> recipient ok 1689717924-N5p8495DYSw0-YqriOY9b
DEBUG SMTP: Verified Addresses
DEBUG SMTP:   gurov@surf.dev
DATA
354 Start mail input, end with <CRLF>.<CRLF>
Date: Tue, 18 Jul 2023 22:05:23 +0000 (UTC)
From: pcserg@yandex.ru
To: gurov@surf.dev
Message-ID: <116057588.19.1689717924523@43be239ec0c2>
Subject: jenkins build:SUCCESS: github/ci
MIME-Version: 1.0
Content-Type: multipart/mixed; 
	boundary="----=_Part_18_369668342.1689717923734"
X-Jenkins-Job: ci
X-Jenkins-Result: SUCCESS
List-ID: 

------=_Part_18_369668342.1689717923734
Content-Type: text/plain; charset=UTF-8
Content-Transfer-Encoding: 7bit

SUCCESS: Job github/ci
More Info can be found here: http://localhost:8080/job/github/job/ci/29/
------=_Part_18_369668342.1689717923734--
.
250 2.0.0 Ok: queued on mail-nwsmtp-smtp-production-main-44.sas.yp-c.yandex.net 1689717924-N5p8495DYSw0-YqriOY9b
DEBUG SMTP: message successfully delivered to mail server
QUIT
221 2.0.0 Closing connecton
```
