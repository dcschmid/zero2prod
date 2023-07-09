How to run:
cargo watch -x check -x test -x run

How to test:

curl -i -X POST -d 'email=thomas_mann3@hotmail.com&name=Tom3' \
http://127.0.0.1:8000/subscriptions

Test health-check

curl -v http://127.0.0.1:8000/health_check

Test send_email

curl "https://api.postmarkapp.com/email" \
-X POST \
-H "Accept: application/json" \
-H "Content-Type: application/json" \
-H "X-Postmark-Server-Token: server token" \
-d '{
"From": "sender@example.com",
"To": "receiver@example.com",
"Subject": "Postmark test",
"TextBody": "Hello dear Postmark user.",
"HtmlBody": "<html><body><strong>Hello</strong> dear Postmark user.</body></html>"
}'