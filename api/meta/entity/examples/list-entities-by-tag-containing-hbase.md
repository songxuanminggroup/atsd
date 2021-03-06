# List Entities Starting with `nur` and with Tag `app` Containing `hbase` 

## Request

### URI

```elm
GET https://atsd_server:8443/api/v1/entities?timeFormat=iso&limit=2&tags=app&expression=name%20LIKE%20%27nur%27%20and%20lower%28tags.app%29%20LIKE%20%27hbase%27
```

### Expression

```
name LIKE 'nur*' and lower(tags.app) LIKE '*hbase*'
```

## Response

```json
[{
    "name": "nurswgvml006",
    "enabled": true,
    "lastInsertDate": "2015-09-04T15:43:36.000Z",
    "tags": {
        "app": "Hadoop/HBASE"
    }
},
{
    "name": "nurswgvml203",
    "enabled": true,
    "tags": {
        "app": "Hadoop/Hbase master node"
    }
}]
```

> 'lower(text)' is a built-in utility string function. 
> Alternatively, any Java string functions can be used to modify the value, for example: 'tags.app.toLowerCase()'
