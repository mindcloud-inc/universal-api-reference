# Atriomail: Update Mailbox



```
PUT https://connect.mindcloud.co/v1/universal/atriomail/latest/actions/update-mailbox
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atriomail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/atriomail/latest/actions/update-mailbox" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mailboxId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/atriomail/latest/actions/update-mailbox', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mailboxId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mailboxId` | number | yes | The AtrioMail mailbox ID. |
| `name` | string | no | The updated mailbox display name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": 1,
      "domain": "string",
      "domainId": 1,
      "id": 1,
      "mailcowId": 1,
      "message": "string",
      "name": "Ava Chen",
      "quota": 1,
      "quotaUsed": 1,
      "syncedAt": "2026-05-07T12:00:00.000Z",
      "syncStatus": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `createdAt` | date |  |
| `createdBy` | number |  |
| `domain` | string |  |
| `domainId` | number |  |
| `id` | number |  |
| `mailcowId` | number |  |
| `message` | string |  |
| `name` | string |  |
| `quota` | number |  |
| `quotaUsed` | number |  |
| `syncedAt` | date |  |
| `syncStatus` | string |  |
| `updatedAt` | date |  |
| `username` | string |  |

## Native endpoint

Through the native Atriomail API, this operation is `PUT /mailboxes/:mailboxId` (base URL `https://system.atriomail.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-mailbox.md) for the provider-specific parameters and requirements.

