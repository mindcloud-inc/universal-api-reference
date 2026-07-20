# LimoExpress: Remove Currency

Removes a currency from the LimoExpress organization.

```
DELETE https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/remove-currency
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LimoExpress `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/remove-currency?connectionId=$CONNECTION_ID&currencyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "currencyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/remove-currency?${params}`, {
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
| `currencyId` | string | yes | Identifier of the currency to remove from the organization. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Operation payload when returned by the API. |
| `message` | string | Operation status or error message. |
| `success` | boolean | Operation success flag when provided by the API. |

## Native endpoint

Through the native LimoExpress API, this operation is `POST /api/integration/remove-currency` (base URL `https://api.limoexpress.me`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-currency.md) for the provider-specific parameters and requirements.

