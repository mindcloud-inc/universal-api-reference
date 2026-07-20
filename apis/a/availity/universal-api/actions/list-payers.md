# Availity: List Payers

Retrieves payers and supported transactions from Availity.

```
GET https://connect.mindcloud.co/v1/universal/availity/latest/actions/list-payers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Availity `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/availity/latest/actions/list-payers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/availity/latest/actions/list-payers?${params}`, {
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
| `payerId` | string | no | Availity-specific payer identifier to narrow the payer list. Example: `BCBSF`. |
| `transactionTypes` | string<string> | no | EDI/HIPAA transaction type code, such as 270, 276, 837P, 837I, or 837D. Accepts multiple values as an array. Example: `270`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "displayName": "Ava Chen",
      "name": "Ava Chen",
      "payerId": "string",
      "processingRoutes": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayName` | string | Payer name as displayed by Availity. |
| `name` | string | Common payer or health plan name. |
| `payerId` | string | Availity-specific payer identifier. |
| `processingRoutes` | object | Available payer transaction routing details. |

## Native endpoint

Through the native Availity API, this operation is `GET /v1/availity-payer-list` (base URL `https://api.availity.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-payers.md) for the provider-specific parameters and requirements.

