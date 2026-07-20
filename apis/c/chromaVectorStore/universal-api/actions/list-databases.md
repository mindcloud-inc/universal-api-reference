# Chroma Vector Store: List Databases

Retrieves tenant database records from Chroma.

```
GET https://connect.mindcloud.co/v1/universal/chromaVectorStore/latest/actions/list-databases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chroma Vector Store `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chromaVectorStore/latest/actions/list-databases?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chromaVectorStore/latest/actions/list-databases?${params}`, {
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
| `limit` | string | no |  |
| `offset` | string | no |  |
| `tenant` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "tenant": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `tenant` | string |  |

## Native endpoint

Through the native Chroma Vector Store API, this operation is `GET /api/v2/tenants/:tenant/databases` (base URL `https://api.trychroma.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-databases.md) for the provider-specific parameters and requirements.

