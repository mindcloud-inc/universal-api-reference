# SparkPost: Update Tracking Domain



```
PUT https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/update-tracking-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SparkPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/update-tracking-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domain": "track-codex-stage3-20260324.net"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/update-tracking-domain', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domain": "track-codex-stage3-20260324.net"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domain` | string | yes | Tracking domain to update. Default: `track-codex-stage3-20260324.net`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "domain": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domain` | string |  |

## Native endpoint

Through the native SparkPost API, this operation is `PUT /tracking-domains/:domain` (base URL `https://api.sparkpost.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-tracking-domain.md) for the provider-specific parameters and requirements.

