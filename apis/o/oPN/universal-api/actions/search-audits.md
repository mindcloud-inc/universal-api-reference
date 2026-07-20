# OPN: Search Audits

Finds audit records in OPN by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/oPN/latest/actions/search-audits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/search-audits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oPN/latest/actions/search-audits?${params}`, {
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
      "actor_email": "ava@example.com",
      "auditable_type": "string",
      "auditable_uid": "string",
      "created_at": "string",
      "description": "string",
      "id": "string",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actor_email` | string |  |
| `auditable_type` | string |  |
| `auditable_uid` | string |  |
| `created_at` | string |  |
| `description` | string |  |
| `id` | string |  |
| `object` | string |  |

## Native endpoint

Through the native OPN API, this operation is `GET /audits/search` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-audits.md) for the provider-specific parameters and requirements.

