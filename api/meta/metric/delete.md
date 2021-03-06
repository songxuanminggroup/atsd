# Metric: Delete

## Description

Delete the specified metric. 

Data collected for the metric will be removed asynchronously in the background.

## Request

| **Method** | **Path** | **Content-Type Header**|
|:---|:---|---:|
| DELETE | `/api/v1/metrics/{metric}` | `application/json` |

### Path Parameters 

|**Name**|**Type**|**Description**|
|:---|:---|:---|
| metric |string|Metric name.|

## Response

### Fields

None.

## Example

### Request

#### URI

```elm
DELETE https://atsd_host:8443/api/v1/metrics/my-metric
```

#### Payload

None.

#### curl

```elm
curl https://atsd_host:8443/api/v1/metrics/my-metric \
  --insecure --verbose --user {username}:{password} \
  --request DELETE
```

### Response

None.

## Additional Examples





