# Envoice: List Supported Payment Providers

Retrieves supported payment providers from Envoice.

```
GET https://connect.mindcloud.co/v1/universal/envoice/latest/actions/list-supported-payment-providers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Envoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/envoice/latest/actions/list-supported-payment-providers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/envoice/latest/actions/list-supported-payment-providers?${params}`, {
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
      "Name": "Ava Chen",
      "SupportedCurrencies": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Name` | string | Payment provider name. |
| `SupportedCurrencies` | array<string> | Currency codes supported by the provider. |

## Native endpoint

Through the native Envoice API, this operation is `GET payment/supported` (base URL `https://www.envoice.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-supported-payment-providers.md) for the provider-specific parameters and requirements.

