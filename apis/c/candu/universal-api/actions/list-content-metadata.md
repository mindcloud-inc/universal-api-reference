# Candu: List Content Metadata

Retrieves content metadata records from Candu.

```
GET https://connect.mindcloud.co/v1/universal/candu/latest/actions/list-content-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Candu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/candu/latest/actions/list-content-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/candu/latest/actions/list-content-metadata?${params}`, {
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
      "name": "Ava Chen",
      "slug": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string | The content name. |
| `slug` | string | The content slug. |

## Native endpoint

Through the native Candu API, this operation is `GET /contentMetadata` (base URL `https://api.candu.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-content-metadata.md) for the provider-specific parameters and requirements.

