# Proofly: List Activity

Retrieves activity events from your Proofly account.

```
GET https://connect.mindcloud.co/v1/universal/proofly/latest/actions/list-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Proofly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proofly/latest/actions/list-activity?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/proofly/latest/actions/list-activity?${params}`, {
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
      "date": "2026-05-07T12:00:00.000Z",
      "ip": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date | Event timestamp |
| `ip` | string | Source IP address |
| `type` | string | Activity event type |

## Native endpoint

Through the native Proofly API, this operation is `GET /activity` (base URL `https://proofly.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-activity.md) for the provider-specific parameters and requirements.

