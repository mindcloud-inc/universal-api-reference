# ClustDoc: List Companies



```
GET https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/list-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClustDoc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/list-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/list-companies?${params}`, {
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
      "address": "string",
      "city": "string",
      "contacts_count": 1,
      "country": "string",
      "id": 1,
      "name": "Ava Chen",
      "phone": "string",
      "state": "string",
      "team_id": 1,
      "website": "string",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `city` | string |  |
| `contacts_count` | number |  |
| `country` | string |  |
| `id` | number |  |
| `name` | string |  |
| `phone` | string |  |
| `state` | string |  |
| `team_id` | number |  |
| `website` | string |  |
| `zip` | string |  |

## Native endpoint

Through the native ClustDoc API, this operation is `GET /companies` (base URL `https://api.clustdoc.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-companies.md) for the provider-specific parameters and requirements.

