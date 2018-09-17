# hm_log


## How to use?

```go
config := make(map[string]string, 8)
config["log_path"] = "."
config["log_name"] = "server"
config["log_chan_size"] = "50000"
config["log_split_type"] = "size"
err := InitLog("file", config) // or err := InitLog("console", config)
if err != nil {
	return
}

for {
	log.Debug("%s", "Debug Test")
	log.Warn("%s", "Warn Test")
	time.Sleep(time.Second)
}
```
