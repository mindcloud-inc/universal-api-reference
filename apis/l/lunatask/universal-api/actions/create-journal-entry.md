# Lunatask: Create Journal Entry



```
POST https://connect.mindcloud.co/v1/universal/lunatask/latest/actions/create-journal-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lunatask `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lunatask/latest/actions/create-journal-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dateOn": "2026-05-07T12:00:00.000Z",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lunatask/latest/actions/create-journal-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dateOn": "2026-05-07T12:00:00.000Z",
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dateOn` | date | yes | ISO-8601 formatted date for the journal entry |
| `name` | string | no | The name for the journal entry |
| `content` | string | yes | The content of the journal entry in Markdown |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dateOn": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `dateOn` | date |  |
| `id` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Lunatask API, this operation is `POST /journal_entries` (base URL `https://api.lunatask.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-journal-entry.md) for the provider-specific parameters and requirements.

