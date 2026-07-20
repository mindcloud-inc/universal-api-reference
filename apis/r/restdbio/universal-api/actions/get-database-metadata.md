# Restdb.io: Get Database Metadata

Retrieves database metadata from Restdb.io.

```
GET https://connect.mindcloud.co/v1/universal/restdbio/latest/actions/get-database-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Restdb.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/restdbio/latest/actions/get-database-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/restdbio/latest/actions/get-database-metadata?${params}`, {
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
      "collections": [
        "string"
      ],
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `collections` | array<string> |  |
| `name` | string |  |

## Native endpoint

Through the native Restdb.io API, this operation is `GET /rest/_meta` (base URL `https://mindcloudstage0-7934.restdb.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-database-metadata.md) for the provider-specific parameters and requirements.

