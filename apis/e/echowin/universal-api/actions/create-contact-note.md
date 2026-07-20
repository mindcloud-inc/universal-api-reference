# echowin: Create Contact Note

Creates a contact note in echowin.

```
POST https://connect.mindcloud.co/v1/universal/echowin/latest/actions/create-contact-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a echowin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/echowin/latest/actions/create-contact-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string",
  "note": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/echowin/latest/actions/create-contact-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "string",
    "note": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | yes |  |
| `note` | string | yes |  |
| `type` | string | no | Default: `GENERAL`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native echowin API returns.

## Native endpoint

Through the native echowin API, this operation is `POST /contacts/:contactId/notes` (base URL `https://echo.win/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact-note.md) for the provider-specific parameters and requirements.

