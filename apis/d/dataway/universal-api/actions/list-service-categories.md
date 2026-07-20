# Dataway: List Service Categories

Retrieves available service categories from Dataway.

```
GET https://connect.mindcloud.co/v1/universal/dataway/latest/actions/list-service-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dataway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataway/latest/actions/list-service-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataway/latest/actions/list-service-categories?${params}`, {
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
      "data": {
        "name": "Ava Chen",
        "slug": "string",
        "status": "string"
      },
      "responseCode": "string",
      "responseDescription": "string",
      "responseMessage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | List of service categories. |
| `data.name` | string | Category display name. |
| `data.slug` | string | Category slug. |
| `data.status` | string | Category status. |
| `responseCode` | string | Provider response code. |
| `responseDescription` | string | Provider response description. |
| `responseMessage` | string | Provider response message. |

## Native endpoint

Through the native Dataway API, this operation is `GET /get-service-categories` (base URL `https://datawayapp.com/vendor`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-service-categories.md) for the provider-specific parameters and requirements.

