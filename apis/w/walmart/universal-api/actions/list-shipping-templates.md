# Walmart: List Shipping Templates

Get all the shipping templates for a Seller.

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/list-shipping-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/list-shipping-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/list-shipping-templates?${params}`, {
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
      "createdDate": 1,
      "id": "string",
      "modifiedDate": 1,
      "name": "Ava Chen",
      "rateModelType": "string",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdDate` | number |  |
| `id` | string |  |
| `modifiedDate` | number |  |
| `name` | string |  |
| `rateModelType` | string |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `GET /v3/settings/shipping/templates` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-shipping-templates.md) for the provider-specific parameters and requirements.

