# node-gateway 

- proxies external requests
- leverages http://expressgateway.io
- uses redis db to store credentials/tokens/users

# run as a service.
- ps -ef | grep node                    # check that it's running
- ps -ef | grep redis

- copy node-gateway.service to /etc/systemd/system/
- systemctl enable node-gateway         # enable auto-start upon reboot of machine

# start app and db
- systemctl start node-gateway
- /etc/init.d/redis_6379 start

# read systemctl start logs
- journalctl -u node-gateway 

# consumers and users credentials/tokens are stored in redis
- https://redis.io/topics/quickstart 
