# Fourthwall: Get Shop Contact Info

Retrieves current shop contact info from Fourthwall.

```
GET https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/get-shop-contact-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fourthwall `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/get-shop-contact-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/get-shop-contact-info?${params}`, {
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
      "contactEmail": "ava@example.com",
      "customerSupportEmail": "ava@example.com",
      "domain": "string",
      "location": {
        "address1": "string",
        "address2": "string",
        "city": "string",
        "country": "string",
        "name": "Ava Chen",
        "state": "string",
        "zip": "string"
      },
      "phone": "string",
      "shopEmail": "ava@example.com",
      "shopName": "Ava Chen",
      "transactionalEmail": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactEmail` | string |  |
| `customerSupportEmail` | string |  |
| `domain` | string |  |
| `location.address1` | string |  |
| `location.address2` | string |  |
| `location.city` | string |  |
| `location.country` | string |  |
| `location.name` | string |  |
| `location.state` | string |  |
| `location.zip` | string |  |
| `phone` | string |  |
| `shopEmail` | string |  |
| `shopName` | string |  |
| `transactionalEmail` | string |  |

## Native endpoint

Through the native Fourthwall API, this operation is `GET /open-api/v1.0/shops/current/contact-info` (base URL `https://api.fourthwall.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shop-contact-info.md) for the provider-specific parameters and requirements.

