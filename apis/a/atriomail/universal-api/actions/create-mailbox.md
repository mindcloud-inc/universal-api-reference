# Atriomail: Create Mailbox



```
POST https://connect.mindcloud.co/v1/universal/atriomail/latest/actions/create-mailbox
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atriomail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/atriomail/latest/actions/create-mailbox" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domainId": 1,
  "localPart": "string",
  "name": "Ava Chen",
  "password": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/atriomail/latest/actions/create-mailbox', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domainId": 1,
    "localPart": "string",
    "name": "Ava Chen",
    "password": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domainId` | number | yes | The AtrioMail domain ID that owns the mailbox. |
| `localPart` | string | yes | The mailbox local part before the @ symbol. |
| `name` | string | yes | The mailbox display name. |
| `password` | string | yes | The mailbox password. |

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

Through the native Atriomail API, this operation is `POST /mailboxes` (base URL `https://system.atriomail.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-mailbox.md) for the provider-specific parameters and requirements.

