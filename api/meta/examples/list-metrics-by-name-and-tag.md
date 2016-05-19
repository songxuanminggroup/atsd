# List metrics by name and tag

List metrics starting with `nmon` and with tag `table` starting with `CPU`

## Request 
### URI 
```elm
GET https://atsd_host:8443/api/v1/metrics?tags=table&limit=2&expression=name%20like%20%27nmon*%27%20and%20tags.table%20like%20%27*CPU*%27&timeFormat=iso
```

### Expression

```
name like 'nmon*' and `tags.table` like '*CPU*'
```

## Response

```json
[
   {
        "name": "nmon.cpu.busy%",
        "enabled": true,
        "dataType": "FLOAT",
        "counter": false,
        "persistent": true,
        "tags": {
            "table": "CPU Detail"
        },
        "timePrecision": "MILLISECONDS",
        "retentionInterval": 0,
        "invalidAction": "NONE",
        "lastInsertDate": "2016-05-19T10:38:26.731Z",
        "versioned": false
    },
    {
        "name": "nmon.cpu.idle%",
        "enabled": true,
        "dataType": "FLOAT",
        "counter": false,
        "persistent": true,
        "tags": {
            "table": "CPU Detail"
        },
        "timePrecision": "MILLISECONDS",
        "retentionInterval": 0,
        "invalidAction": "NONE",
        "lastInsertDate": "2016-05-19T10:38:26.731Z",
        "versioned": false
    }
]
```