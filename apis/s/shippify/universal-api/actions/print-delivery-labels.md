# Shippify: Print Delivery Labels

Retrieves PDF delivery labels from Shippify.

```
GET https://connect.mindcloud.co/v1/universal/shippify/latest/actions/print-delivery-labels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shippify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shippify/latest/actions/print-delivery-labels?connectionId=$CONNECTION_ID&deliveryIds%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "deliveryIds[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shippify/latest/actions/print-delivery-labels?${params}`, {
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
| `deliveryIds[]` | array<string> | yes | Required array of Shippify delivery identifiers whose labels should be generated. |
| `referenceIds[]` | array<string> | no | Optional array of Shippify delivery reference identifiers whose labels should be generated. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string | Generated PDF document containing delivery labels. |

## Native endpoint

Through the native Shippify API, this operation is `POST /v2/integrations/deliveries/labels` (base URL `https://api.shippify.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/print-delivery-labels.md) for the provider-specific parameters and requirements.

