# Column: List Financial Institutions



```
GET https://connect.mindcloud.co/v1/universal/column/latest/actions/list-financial-institutions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Column `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/column/latest/actions/list-financial-institutions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/column/latest/actions/list-financial-institutions?${params}`, {
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
| `countryCode` | string | no | ISO 3166-1 Alpha-2 country code for institution filtering. |
| `name` | string | no | Case-insensitive keywords in institution full names. |
| `routingNumberType` | string | no | Routing number type filter: aba or bic. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "achEligible": true,
      "checkEligible": true,
      "city": "string",
      "countryCode": "string",
      "createdAt": "string",
      "fullName": "Ava Chen",
      "phoneNumber": "string",
      "realtimeEligible": true,
      "realtimeRfpEligible": true,
      "routingNumber": "string",
      "routingNumberType": "string",
      "shortName": "Ava Chen",
      "state": "string",
      "streetAddress": "string",
      "updatedAt": "string",
      "wireEligible": true,
      "wireSettlementOnly": true,
      "zipCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `achEligible` | boolean |  |
| `checkEligible` | boolean |  |
| `city` | string |  |
| `countryCode` | string |  |
| `createdAt` | string |  |
| `fullName` | string |  |
| `phoneNumber` | string |  |
| `realtimeEligible` | boolean |  |
| `realtimeRfpEligible` | boolean |  |
| `routingNumber` | string |  |
| `routingNumberType` | string |  |
| `shortName` | string |  |
| `state` | string |  |
| `streetAddress` | string |  |
| `updatedAt` | string |  |
| `wireEligible` | boolean |  |
| `wireSettlementOnly` | boolean |  |
| `zipCode` | string |  |

## Native endpoint

Through the native Column API, this operation is `GET /institutions` (base URL `https://api.column.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-financial-institutions.md) for the provider-specific parameters and requirements.

