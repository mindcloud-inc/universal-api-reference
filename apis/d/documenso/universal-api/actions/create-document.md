# Documenso: Create Document

Creates a new document in Documenso.

```
POST https://connect.mindcloud.co/v1/universal/documenso/latest/actions/create-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documenso `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/documenso/latest/actions/create-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "payload": {},
  "files": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documenso/latest/actions/create-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "payload": {},
    "files": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `payload` | object | yes |  |
| `files` | file | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Documenso API, this operation is `POST /envelope/create` (base URL `https://app.documenso.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document.md) for the provider-specific parameters and requirements.

