# Better Proposals: Get Currency Details

Retrieves currency details from Better Proposals.

```
GET https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/get-currency-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Proposals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/get-currency-details?connectionId=$CONNECTION_ID&currencyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "currencyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/get-currency-details?${params}`, {
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
| `currencyId` | string | yes | The Better Proposals currency ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currencyCode": "string",
      "currencyName": "Ava Chen",
      "currencySymbol": "string",
      "id": "string",
      "paypalSupport": "string",
      "stripeSupport": "string",
      "zeroDecimal": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currencyCode` | string |  |
| `currencyName` | string |  |
| `currencySymbol` | string |  |
| `id` | string |  |
| `paypalSupport` | string |  |
| `stripeSupport` | string |  |
| `zeroDecimal` | string |  |

## Native endpoint

Through the native Better Proposals API, this operation is `GET /currency/:CURRENCY_ID` (base URL `https://api.betterproposals.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-currency-details.md) for the provider-specific parameters and requirements.

