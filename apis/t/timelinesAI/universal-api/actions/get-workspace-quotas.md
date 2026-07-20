# TimelinesAI: Get Workspace Quotas

Retrieves workspace quotas and usage from TimelinesAI.

```
GET https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/get-workspace-quotas
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TimelinesAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/get-workspace-quotas?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/get-workspace-quotas?${params}`, {
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
        "messagingQuota": {
          "periodEnd": "string",
          "periodStart": "string",
          "total": 1,
          "used": 1
        },
        "seats": {
          "periodEnd": "string",
          "periodStart": "string",
          "total": 1,
          "used": 1
        }
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.messagingQuota` | object |  |
| `data.messagingQuota.periodEnd` | string |  |
| `data.messagingQuota.periodStart` | string |  |
| `data.messagingQuota.total` | number |  |
| `data.messagingQuota.used` | number |  |
| `data.seats` | object |  |
| `data.seats.periodEnd` | string |  |
| `data.seats.periodStart` | string |  |
| `data.seats.total` | number |  |
| `data.seats.used` | number |  |
| `status` | string |  |

## Native endpoint

Through the native TimelinesAI API, this operation is `GET /quotas` (base URL `https://app.timelines.ai/integrations/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace-quotas.md) for the provider-specific parameters and requirements.

