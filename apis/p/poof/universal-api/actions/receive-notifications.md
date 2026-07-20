# Poof: Receive Notifications

Creates a new webhook in Poof.

```
POST https://connect.mindcloud.co/v1/universal/poof/latest/actions/receive-notifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Poof `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/poof/latest/actions/receive-notifications" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://www.poof.io/example_route"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/poof/latest/actions/receive-notifications', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://www.poof.io/example_route"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Webhook callback URL. Default: `https://www.poof.io/example_route`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endpoint": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endpoint` | string |  |
| `message` | string |  |

## Native endpoint

Through the native Poof API, this operation is `POST https://www.poof.io/api/v1/create_webhook` (base URL `https://www.poof.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/receive-notifications.md) for the provider-specific parameters and requirements.

