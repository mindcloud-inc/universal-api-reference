# Eversign: List Businesses

Retrieves business records from your Eversign account.

```
GET https://connect.mindcloud.co/v1/universal/eversign/latest/actions/list-businesses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eversign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eversign/latest/actions/list-businesses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eversign/latest/actions/list-businesses?${params}`, {
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
      "business_connection_id": "string",
      "business_id": 1,
      "business_identifier": "string",
      "business_name": "Ava Chen",
      "business_status": 1,
      "creation_time_stamp": 1,
      "is_primary": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `business_connection_id` | string |  |
| `business_id` | number |  |
| `business_identifier` | string |  |
| `business_name` | string |  |
| `business_status` | number |  |
| `creation_time_stamp` | number |  |
| `is_primary` | number |  |

## Native endpoint

Through the native Eversign API, this operation is `GET /business` (base URL `https://api.eversign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-businesses.md) for the provider-specific parameters and requirements.

