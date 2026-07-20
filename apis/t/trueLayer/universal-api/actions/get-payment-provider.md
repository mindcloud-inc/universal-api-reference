# TrueLayer: Get Payment Provider

Retrieves a payment provider from TrueLayer.

```
GET https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/get-payment-provider
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrueLayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/get-payment-provider?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/get-payment-provider?${params}`, {
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
| `id` | string | yes | TrueLayer payment provider ID, such as mock-payments-gb-redirect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "countries": [
        "string"
      ],
      "display_name": "Ava Chen",
      "icon_uri": "string",
      "id": "string",
      "schemes": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `countries` | array<string> |  |
| `display_name` | string |  |
| `icon_uri` | string |  |
| `id` | string |  |
| `schemes` | array<object> |  |

## Native endpoint

Through the native TrueLayer API, this operation is `GET /v3/payments-providers/:id` (base URL `https://api.truelayer-sandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-payment-provider.md) for the provider-specific parameters and requirements.

