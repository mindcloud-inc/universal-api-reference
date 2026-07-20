# Understory: List Marketing Consents

Retrieves marketing consents from Understory.

```
GET https://connect.mindcloud.co/v1/universal/understory/latest/actions/list-marketing-consents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Understory `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/understory/latest/actions/list-marketing-consents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/understory/latest/actions/list-marketing-consents?${params}`, {
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
      "items": [
        {
          "company_id": "string",
          "email": "ava@example.com",
          "full_name": "Ava Chen",
          "source": "string"
        }
      ],
      "next": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[].company_id` | string |  |
| `items[].email` | string |  |
| `items[].full_name` | string |  |
| `items[].source` | string |  |
| `next` | string |  |

## Native endpoint

Through the native Understory API, this operation is `GET /v1/marketing-consents` (base URL `https://api.understory.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-marketing-consents.md) for the provider-specific parameters and requirements.

