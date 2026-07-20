# VentiPay: List Customers

Retrieves customers from VentiPay.

```
GET https://connect.mindcloud.co/v1/universal/ventiPay/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VentiPay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ventiPay/latest/actions/list-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ventiPay/latest/actions/list-customers?${params}`, {
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
| `email` | string | no | Email del cliente. Debe ser coincidencia exacta. |
| `country` | string | no | País del cliente en formato ISO 3166-1 alpha-2. |
| `startingAfter` | string | no | Return records after this pagination cursor from a previous response. |
| `endingBefore` | string | no | Return records before this pagination cursor from a previous response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "has_more": true,
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Customer records returned by the list request. |
| `has_more` | boolean | Whether more customer records are available beyond this page. |
| `object` | string | Response object type. |

## Native endpoint

Through the native VentiPay API, this operation is `GET /customers` (base URL `https://api.ventipay.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

