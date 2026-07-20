# Cloudprinter.com: List Shipping Levels

Retrieves shipping levels from Cloudprinter.com.

```
GET https://connect.mindcloud.co/v1/universal/cloudprintercom/latest/actions/list-shipping-levels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudprinter.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudprintercom/latest/actions/list-shipping-levels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudprintercom/latest/actions/list-shipping-levels?${params}`, {
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
      "note": "string",
      "shipping_level": "string",
      "shipping_level_reference": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `note` | string |  |
| `shipping_level` | string |  |
| `shipping_level_reference` | string |  |

## Native endpoint

Through the native Cloudprinter.com API, this operation is `POST /cloudcore/1.0/shipping/levels` (base URL `https://api.cloudprinter.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-shipping-levels.md) for the provider-specific parameters and requirements.

