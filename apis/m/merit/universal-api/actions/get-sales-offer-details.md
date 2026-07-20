# Merit: Get Sales Offer Details



```
GET https://connect.mindcloud.co/v1/universal/merit/latest/actions/get-sales-offer-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Merit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/merit/latest/actions/get-sales-offer-details?connectionId=$CONNECTION_ID&Id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "Id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/merit/latest/actions/get-sales-offer-details?${params}`, {
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
| `Id` | string | yes | Sales offer ID from Merit docs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CustomerId": "string",
      "CustomerName": "Ava Chen",
      "DocDate": "2026-05-07T12:00:00.000Z",
      "OfferId": "string",
      "OfferNo": "string",
      "OfferRow": [
        {}
      ],
      "TaxAmount": 1,
      "TotalAmount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CustomerId` | string |  |
| `CustomerName` | string |  |
| `DocDate` | date |  |
| `OfferId` | string |  |
| `OfferNo` | string |  |
| `OfferRow` | array<object> |  |
| `TaxAmount` | number |  |
| `TotalAmount` | number |  |

## Native endpoint

Through the native Merit API, this operation is `POST v2/getoffer` (base URL `https://aktiva.merit.ee/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sales-offer-details.md) for the provider-specific parameters and requirements.

