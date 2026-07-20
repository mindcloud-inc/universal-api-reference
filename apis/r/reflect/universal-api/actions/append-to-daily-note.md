# Reflect: Append to Daily Note

Appends text to a daily note in Reflect.

```
PUT https://connect.mindcloud.co/v1/universal/reflect/latest/actions/append-to-daily-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reflect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/reflect/latest/actions/append-to-daily-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "graphId": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reflect/latest/actions/append-to-daily-note', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "graphId": "string",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `graphId` | list<string> | yes | Your graph identifier |
| `date` | date | no | Date of the daily note in ISO 8601 format |
| `text` | string | yes | Text to append to the daily note |
| `listName` | string | no | Name of the list to append to |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Reflect API, this operation is `PUT /graphs/:graphId/daily-notes` (base URL `https://reflect.app/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/append-to-daily-note.md) for the provider-specific parameters and requirements.

