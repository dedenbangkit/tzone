# tzone - A simple CLI timezone visualizer.

![cover](https://repository-images.githubusercontent.com/231573820/44893b00-2e5a-11ea-9709-b59e3f48a3c3)

#### Installation

```bash
go get "github.com/dedenbangkit/tzone"
```

#### Usage
```
tzone list
tzone [zones] [--date] [--24]

examples:
  tzone UTC
  tzone UTC,Local
  tzone Asia/Jakarta
  tzone Asia/Jakarta:Deden
  tzone Asia/Jakarta:Deden:9:17
  tzone UTC,Asia/Jakarta:Deden:9:17
```

Zone format is a comma delimited set of:

```
<timezone>[:name][:start time][:end time]
```

You can set YAML zones in your home directory `~/.tzone`:

```
- tz: "UTC"
- tz: "local"
  name: "Deden"
  start: 9 
  end: 17
```


You can also set via envrionment variables:

```
TZ_ZONES="UTC,Asia/Jakarta:Matt:8:17,Asia/Jakarta:Deden:8:17"
TZ_24=true
TZ_DATE=true
```

![example](https://raw.githubusercontent.com/dedenbangkit/tzone/master/example.png)

