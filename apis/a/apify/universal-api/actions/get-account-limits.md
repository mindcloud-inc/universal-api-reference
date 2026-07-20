# Apify: Get Account Limits

Retrieves account limits from Apify.

```
GET https://connect.mindcloud.co/v1/universal/apify/latest/actions/get-account-limits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apify/latest/actions/get-account-limits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apify/latest/actions/get-account-limits?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "current": {
          "activeActorJobCount": 1,
          "actorCount": 1,
          "actorMemoryGbytes": 1,
          "actorTaskCount": 1,
          "monthlyActorComputeUnits": 1,
          "monthlyExternalDataTransferGbytes": 1,
          "monthlyProxySerps": 1,
          "monthlyResidentialProxyGbytes": 1,
          "monthlyUsageUsd": 1,
          "scheduleCount": 1,
          "teamAccountSeatCount": 1
        },
        "limits": {
          "dataRetentionDays": 1,
          "maxActorCount": 1,
          "maxActorMemoryGbytes": 1,
          "maxActorTaskCount": 1,
          "maxConcurrentActorJobs": 1,
          "maxMonthlyActorComputeUnits": 1,
          "maxMonthlyExternalDataTransferGbytes": 1,
          "maxMonthlyProxySerps": 1,
          "maxMonthlyResidentialProxyGbytes": 1,
          "maxMonthlyUsageUsd": 1,
          "maxScheduleCount": 1,
          "maxTeamAccountSeatCount": 1
        },
        "monthlyUsageCycle": {
          "endAt": "string",
          "startAt": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.current.activeActorJobCount` | number |  |
| `data.current.actorCount` | number |  |
| `data.current.actorMemoryGbytes` | number |  |
| `data.current.actorTaskCount` | number |  |
| `data.current.monthlyActorComputeUnits` | number |  |
| `data.current.monthlyExternalDataTransferGbytes` | number |  |
| `data.current.monthlyProxySerps` | number |  |
| `data.current.monthlyResidentialProxyGbytes` | number |  |
| `data.current.monthlyUsageUsd` | number |  |
| `data.current.scheduleCount` | number |  |
| `data.current.teamAccountSeatCount` | number |  |
| `data.limits.dataRetentionDays` | number |  |
| `data.limits.maxActorCount` | number |  |
| `data.limits.maxActorMemoryGbytes` | number |  |
| `data.limits.maxActorTaskCount` | number |  |
| `data.limits.maxConcurrentActorJobs` | number |  |
| `data.limits.maxMonthlyActorComputeUnits` | number |  |
| `data.limits.maxMonthlyExternalDataTransferGbytes` | number |  |
| `data.limits.maxMonthlyProxySerps` | number |  |
| `data.limits.maxMonthlyResidentialProxyGbytes` | number |  |
| `data.limits.maxMonthlyUsageUsd` | number |  |
| `data.limits.maxScheduleCount` | number |  |
| `data.limits.maxTeamAccountSeatCount` | number |  |
| `data.monthlyUsageCycle.endAt` | string |  |
| `data.monthlyUsageCycle.startAt` | string |  |

## Native endpoint

Through the native Apify API, this operation is `GET /v2/users/me/limits` (base URL `https://api.apify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-limits.md) for the provider-specific parameters and requirements.

