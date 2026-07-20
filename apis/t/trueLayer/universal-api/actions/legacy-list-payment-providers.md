# TrueLayer: Legacy List Payment Providers

Retrieves legacy payment providers from TrueLayer.

```
GET https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/legacy-list-payment-providers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrueLayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/legacy-list-payment-providers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/legacy-list-payment-providers?${params}`, {
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
      "capabilities": [
        "string"
      ],
      "country": "string",
      "display_name": "Ava Chen",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capabilities` | array<string> |  |
| `country` | string |  |
| `display_name` | string |  |
| `id` | string |  |

## Native endpoint

Through the native TrueLayer API, this operation is `GET /v2/single-immediate-payments-providers` (base URL `https://api.truelayer-sandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/legacy-list-payment-providers.md) for the provider-specific parameters and requirements.

