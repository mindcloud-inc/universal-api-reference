# echowin: Update Contact Boards

Updates contact boards in echowin.

```
PUT https://connect.mindcloud.co/v1/universal/echowin/latest/actions/update-contact-boards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a echowin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/echowin/latest/actions/update-contact-boards" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string",
  "boardIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/echowin/latest/actions/update-contact-boards', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "string",
    "boardIds[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | yes |  |
| `boardIds[]` | array<string> | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native echowin API returns.

## Native endpoint

Through the native echowin API, this operation is `PUT /contacts/:contactId/boards` (base URL `https://echo.win/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact-boards.md) for the provider-specific parameters and requirements.

