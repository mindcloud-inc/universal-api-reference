# Oanda: Get Supported Forwards

Retrieves supported forward tenors from Oanda.

```
GET https://connect.mindcloud.co/v1/universal/oanda/latest/actions/get-supported-forwards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Oanda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oanda/latest/actions/get-supported-forwards?connectionId=$CONNECTION_ID&ext=json" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ext": "json"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oanda/latest/actions/get-supported-forwards?${params}`, {
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
| `base` | string | no | Base currency or comma-separated list. |
| `data_set` | string | no | Dataset code. |
| `ext` | string | yes | Response format. Default: `json`. |
| `quote` | string | no | Quote currency or comma-separated list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "supported_forwards": [
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
| `supported_forwards` | array<object> | Supported forward tenors per currency pair. |

## Native endpoint

Through the native Oanda API, this operation is `GET /v2/supported_forwards.:ext` (base URL `https://exchange-rates-api.oanda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-supported-forwards.md) for the provider-specific parameters and requirements.

