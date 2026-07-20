# Laposta: Create Subscriber

Creates a new subscriber in Laposta.

```
POST https://connect.mindcloud.co/v1/universal/laposta/latest/actions/create-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Laposta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/laposta/latest/actions/create-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": "string",
  "ip": "string",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/laposta/latest/actions/create-subscriber', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": "string",
    "ip": "string",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listId` | string | yes | The ID of the list to add the subscriber to. |
| `ip` | string | yes | The IP address from which the subscriber is registered. |
| `email` | string | yes | Subscriber email address. |
| `sourceUrl` | string | no | The URL from which the subscriber signed up. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "member": {
        "email": "ava@example.com",
        "listId": "string",
        "memberId": "string",
        "signupDate": "string",
        "sourceUrl": "https://example.com",
        "state": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `member` | object |  |
| `member.email` | string |  |
| `member.listId` | string |  |
| `member.memberId` | string |  |
| `member.signupDate` | string |  |
| `member.sourceUrl` | string |  |
| `member.state` | string |  |

## Native endpoint

Through the native Laposta API, this operation is `POST /member` (base URL `https://api.laposta.nl/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-subscriber.md) for the provider-specific parameters and requirements.

