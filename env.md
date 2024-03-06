DATABASE_URL="USER:PASSWORD@tcp(IP:PORT)/DATABASE_NAME?parseTime=true"

The `parseTime` argument is not supposed to be used by `goose`. So in Github Secrets for `DATABASE_URL` remove that argument. Do this *only* if you have to use `port` in the value.
You will have to comment out the `addParseTimeParam` part in `main.go` and all the other corresponding parts. Assign `dbURL` to `parsedURL`.

Otherwise it seems only using the ip address without the port number also does the trick
