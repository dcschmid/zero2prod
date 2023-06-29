How to run:
cargo watch -x check -x test -x run

How to test:

curl -i -X POST -d 'email=thomas_mann3@hotmail.com&name=Tom3' \
http://127.0.0.1:8000/subscriptions

Test health-check

curl -v http://127.0.0.1:8000/health_check
