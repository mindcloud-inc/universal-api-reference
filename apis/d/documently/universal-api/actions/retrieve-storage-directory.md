# Documently: Retrieve Storage Directory

Retrieves a storage directory from Documently.

```
GET https://connect.mindcloud.co/v1/universal/documently/latest/actions/retrieve-storage-directory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documently `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documently/latest/actions/retrieve-storage-directory?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documently/latest/actions/retrieve-storage-directory?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `directoryId` | string | no | The storage directory id. |

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

Through the native Documently API, this operation is `GET /storage-directories/:directoryId` (base URL `https://app.documently.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-storage-directory.md) for the provider-specific parameters and requirements.

