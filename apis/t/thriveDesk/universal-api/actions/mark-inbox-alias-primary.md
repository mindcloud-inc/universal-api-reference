# ThriveDesk: Mark Inbox Alias Primary



```
PUT https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/mark-inbox-alias-primary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ThriveDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/mark-inbox-alias-primary" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "aliasId": "string",
  "inboxId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/mark-inbox-alias-primary', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "aliasId": "string",
    "inboxId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `aliasId` | string | yes | The alias ID. |
| `inboxId` | string | yes | The inbox ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Raw inbox payload. |
| `email` | string | Inbox email address when returned. |
| `id` | string | Inbox identifier. |
| `name` | string | Inbox name when returned. |

## Native endpoint

Through the native ThriveDesk API, this operation is `PATCH /v1/settings/inbox/{{inboxId}}/aliases/{{aliasId}}/mark-as-primary` (base URL `https://api.thrivedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-inbox-alias-primary.md) for the provider-specific parameters and requirements.

