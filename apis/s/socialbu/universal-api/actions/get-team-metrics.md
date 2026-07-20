# Socialbu: Get Team Metrics

Retrieves team metrics from SocialBu insights.

```
GET https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/get-team-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socialbu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/get-team-metrics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/get-team-metrics?${params}`, {
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
      "end": "string",
      "metrics": {},
      "start": "string",
      "team": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `end` | string |  |
| `metrics` | object |  |
| `start` | string |  |
| `team` | object |  |

## Native endpoint

Through the native Socialbu API, this operation is `GET /insights/teams/metrics` (base URL `https://socialbu.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team-metrics.md) for the provider-specific parameters and requirements.

