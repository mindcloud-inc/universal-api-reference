# Merit: List Sales Offers



```
GET https://connect.mindcloud.co/v1/universal/merit/latest/actions/list-sales-offers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Merit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/merit/latest/actions/list-sales-offers?connectionId=$CONNECTION_ID&PeriodStart=20260401&PeriodEnd=20260430" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "PeriodStart": "20260401",
  "PeriodEnd": "20260430"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/merit/latest/actions/list-sales-offers?${params}`, {
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
| `PeriodStart` | string | yes | Start date in YYYYmmdd from Merit docs. Example: `20260401`. |
| `PeriodEnd` | string | yes | End date in YYYYmmdd from Merit docs. Example: `20260430`. |
| `DateType` | number | no | 0=document date, 1=changed date. Default: `0`. |
| `UnPaid` | boolean | no | Filter unpaid sales offers only. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CustomerId": "string",
      "CustomerName": "Ava Chen",
      "DocStatus": 1,
      "DocumentDate": "2026-05-07T12:00:00.000Z",
      "OfferNo": "string",
      "SIHId": "string",
      "TotalSum": 1
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
| `DocStatus` | number |  |
| `DocumentDate` | date |  |
| `OfferNo` | string |  |
| `SIHId` | string |  |
| `TotalSum` | number |  |

## Native endpoint

Through the native Merit API, this operation is `POST v2/getoffers` (base URL `https://aktiva.merit.ee/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sales-offers.md) for the provider-specific parameters and requirements.

