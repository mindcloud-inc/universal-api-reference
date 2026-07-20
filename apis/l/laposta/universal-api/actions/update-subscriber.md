# Laposta: Update Subscriber

Updates an existing subscriber in Laposta.

```
PUT https://connect.mindcloud.co/v1/universal/laposta/latest/actions/update-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Laposta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/laposta/latest/actions/update-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "memberId": "string",
  "listId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/laposta/latest/actions/update-subscriber', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "memberId": "string",
    "listId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `memberId` | string | yes | The subscriber ID or email address to update. |
| `listId` | string | yes | The ID of the list that owns the subscriber. |
| `email` | string | no | Updated subscriber email address. |
| `state` | list | no | Updated subscriber state. One of: `active`, `unsubscribed`. |

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

Through the native Laposta API, this operation is `POST /member/:memberId` (base URL `https://api.laposta.nl/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-subscriber.md) for the provider-specific parameters and requirements.

