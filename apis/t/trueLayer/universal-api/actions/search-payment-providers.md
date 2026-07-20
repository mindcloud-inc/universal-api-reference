# TrueLayer: Search Payment Providers

Searches payment providers in TrueLayer.

```
GET https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/search-payment-providers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrueLayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/search-payment-providers?connectionId=$CONNECTION_ID&countries%5B%5D=string&currencies%5B%5D=string&authorization_flow=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "countries[]": "string",
  "currencies[]": "string",
  "authorization_flow": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/search-payment-providers?${params}`, {
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
| `countries[]` | array<string> | yes | ISO 3166-1 alpha-2 country codes to search payment providers for, such as GB. |
| `currencies[]` | array<string> | yes | ISO 4217 currency codes to search payment providers for, such as GBP. |
| `authorization_flow` | object | yes | Authorization flow filter. Example: {"configuration":{"redirect":{}}}. |

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

Through the native TrueLayer API, this operation is `POST /v3/payments-providers/search` (base URL `https://api.truelayer-sandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-payment-providers.md) for the provider-specific parameters and requirements.

