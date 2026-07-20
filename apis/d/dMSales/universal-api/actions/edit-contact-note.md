# DMSales: Edit Contact Note

Updates an existing contact note in DMSales.

```
PUT https://connect.mindcloud.co/v1/universal/dMSales/latest/actions/edit-contact-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DMSales `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dMSales/latest/actions/edit-contact-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "baseKey": "string",
  "noteId": "string",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dMSales/latest/actions/edit-contact-note', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "baseKey": "string",
    "noteId": "string",
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tag` | string | no | Optional note tag. |
| `baseKey` | string | yes | Contact base key. |
| `noteId` | string | yes | Note UUID to edit. |
| `content` | string | yes | Updated note content. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native DMSales API, this operation is `POST /api/contact-card/edit-note` (base URL `https://app.dmsales.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/edit-contact-note.md) for the provider-specific parameters and requirements.

