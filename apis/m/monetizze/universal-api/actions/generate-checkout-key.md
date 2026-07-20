# Monetizze: Generate Checkout Key

Retrieves a transparent checkout key from Monetizze.

```
GET https://connect.mindcloud.co/v1/universal/monetizze/latest/actions/generate-checkout-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Monetizze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monetizze/latest/actions/generate-checkout-key?connectionId=$CONNECTION_ID&ctk=string&reference=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ctk": "string",
  "reference": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monetizze/latest/actions/generate-checkout-key?${params}`, {
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
| `ctk` | string | yes | Checkout transparent CTK environment key. |
| `reference` | string | yes | Product checkout reference used by Monetizze. |
| `ipAddress` | string | no | Optional buyer IP address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Raw HTML or text response returned by the transparent checkout key endpoint. |

## Native endpoint

Through the native Monetizze API, this operation is `GET https://app.monetizze.com.br/checkout/transparente/js` (base URL `https://api.monetizze.com.br/2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-checkout-key.md) for the provider-specific parameters and requirements.

