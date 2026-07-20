# Documently: Update Storage Directory

Updates an existing storage directory in Documently.

```
PUT https://connect.mindcloud.co/v1/universal/documently/latest/actions/update-storage-directory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documently `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/documently/latest/actions/update-storage-directory" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documently/latest/actions/update-storage-directory', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `directoryId` | string | no | The storage directory id. |
| `name` | string | no | Directory name. |
| `project` | string | no | Project ID for the directory. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@context": "string",
      "@id": "string",
      "@type": "string",
      "children": [
        {}
      ],
      "id": "string",
      "metadata": {},
      "name": "Ava Chen",
      "project": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@context` | string |  |
| `@id` | string |  |
| `@type` | string |  |
| `children` | array<object> |  |
| `id` | string |  |
| `metadata` | object |  |
| `name` | string |  |
| `project` | string |  |

## Native endpoint

Through the native Documently API, this operation is `PATCH /storage-directories/:directoryId` (base URL `https://app.documently.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-storage-directory.md) for the provider-specific parameters and requirements.

