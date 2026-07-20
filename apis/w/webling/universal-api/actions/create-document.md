# Webling: Create Document



```
POST https://connect.mindcloud.co/v1/universal/webling/latest/actions/create-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webling/latest/actions/create-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "stage3.txt",
  "parentId": "259",
  "fileContent": "U3RhZ2UgMyBkb2N1bWVudCBjb250ZW50"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webling/latest/actions/create-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "stage3.txt",
    "parentId": "259",
    "fileContent": "U3RhZ2UgMyBkb2N1bWVudCBjb250ZW50"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Document title, including the filename and extension Webling should store. Example: `stage3.txt`. |
| `parentId` | number | yes | Documentgroup ID that should own the new document. Default: `259`. |
| `fileContent` | string | yes | Base64-encoded file content for the new document. Example: `U3RhZ2UgMyBkb2N1bWVudCBjb250ZW50`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |

## Native endpoint

Through the native Webling API, this operation is `POST /document` (base URL `https://{{credentials.instanceDomain}}/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document.md) for the provider-specific parameters and requirements.

