# XPS Ship: Retrieve Shipping Label

Retrieves a shipping label from XPS Ship.

```
GET https://connect.mindcloud.co/v1/universal/xPSShip/latest/actions/retrieve-shipping-label
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XPS Ship `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xPSShip/latest/actions/retrieve-shipping-label?connectionId=$CONNECTION_ID&bookNumber=string&labelImageFormat=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bookNumber": "string",
  "labelImageFormat": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xPSShip/latest/actions/retrieve-shipping-label?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bookNumber` | string | yes | XPS Ship shipment book number. |
| `labelImageFormat` | string | yes | Requested label format, PDF or PNG. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "base64Images": [
        "string"
      ],
      "labelImageFormat": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `base64Images` | array<string> |  |
| `labelImageFormat` | string |  |

## Native endpoint

Through the native XPS Ship API, this operation is `GET /restapi/v1/customers/:customerId/shipments/:bookNumber/label/:labelImageFormat` (base URL `https://xpsshipper.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-shipping-label.md) for the provider-specific parameters and requirements.

