# Xodo Sign: List Businesses

Retrieves businesses from Xodo Sign.

```
GET https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/list-businesses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xodo Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/list-businesses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/list-businesses?${params}`, {
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
| `business_connection_id` | string | Business connection identifier returned by the API. |
| `business_id` | number | Business ID returned by Xodo Sign. |
| `business_identifier` | string | Workspace subdomain identifier for the business. |
| `business_name` | string | Display name of the business. |
| `business_status` | number | Business status code for the business. |
| `creation_time_stamp` | number | Business creation time as a Unix timestamp. |
| `is_primary` | number | Whether the business is the primary business (1) or not (0). |

## Native endpoint

Through the native Xodo Sign API, this operation is `GET /business` (base URL `https://api.eversign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-businesses.md) for the provider-specific parameters and requirements.

