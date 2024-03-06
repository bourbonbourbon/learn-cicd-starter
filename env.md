DATABASE_URL="user:password@tcp(ip:port)/database_name?parseTime=true"

The `parseTime` argument is not supposed to be used by `goose`. So in Github Secrets for `DATABASE_URL` remove that argument. Do this only if you have to use `port` in the value
