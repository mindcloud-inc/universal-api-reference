# Chroma Cloud: Get collection by ID

Retrieves a collection by ID from Chroma Cloud.

```
GET https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/get-collection-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chroma Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/get-collection-by-id?connectionId=$CONNECTION_ID&collectionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collectionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/get-collection-by-id?${params}`, {
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
| `collectionId` | string | yes | Collection UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "database": "string",
      "dimension": 1,
      "id": "string",
      "metadata": {},
      "name": "Ava Chen",
      "tenant": "string",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `database` | string |  |
| `dimension` | number |  |
| `id` | string |  |
| `metadata` | object |  |
| `name` | string |  |
| `tenant` | string |  |
| `version` | number |  |

## Native endpoint

Through the native Chroma Cloud API, this operation is `GET /api/v2/tenants/:tenant/databases/:database/collections/by-id/:collection_id` (base URL `https://api.trychroma.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-collection-by-id.md) for the provider-specific parameters and requirements.

