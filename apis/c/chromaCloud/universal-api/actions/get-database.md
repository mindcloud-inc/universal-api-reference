# Chroma Cloud: Get database

Retrieves a database from Chroma Cloud.

```
GET https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/get-database
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chroma Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/get-database?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/get-database?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Chroma Cloud API, this operation is `GET /api/v2/tenants/:tenant/databases/:database` (base URL `https://api.trychroma.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-database.md) for the provider-specific parameters and requirements.

