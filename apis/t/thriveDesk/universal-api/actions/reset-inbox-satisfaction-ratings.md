# ThriveDesk: Reset Inbox Satisfaction Ratings



```
PUT https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/reset-inbox-satisfaction-ratings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ThriveDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/reset-inbox-satisfaction-ratings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inboxId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/reset-inbox-satisfaction-ratings', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inboxId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inboxId` | string | yes | The inbox ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "id": "string",
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Raw response payload when returned. |
| `id` | string | Affected record identifier when returned. |
| `message` | string | Provider response message when returned. |
| `success` | boolean | Whether the request completed successfully. |

## Native endpoint

Through the native ThriveDesk API, this operation is `POST /v1/settings/inbox/{{inboxId}}/satisfaction-ratings/reset` (base URL `https://api.thrivedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reset-inbox-satisfaction-ratings.md) for the provider-specific parameters and requirements.

