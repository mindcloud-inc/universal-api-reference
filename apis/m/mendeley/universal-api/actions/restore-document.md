# Mendeley: Restore Document



```
PUT https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/restore-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendeley `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/restore-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/restore-document', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Identifier (UUID) of the document. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Mendeley API returns.

## Native endpoint

Through the native Mendeley API, this operation is `POST /trash/:id/restore` (base URL `https://api.mendeley.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/restore-document.md) for the provider-specific parameters and requirements.

