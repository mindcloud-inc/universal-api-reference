# Stax: Get Deposit Details

Retrieves details for a deposit in Stax.

```
GET https://connect.mindcloud.co/v1/universal/stax/latest/actions/get-deposit-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stax/latest/actions/get-deposit-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stax/latest/actions/get-deposit-details?${params}`, {
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
| `endDate` | string | no | Deposit detail report end date |
| `id` | string | no | Deposit identifier |
| `startDate` | string | no | Deposit detail report start date |
| `timespan` | string | no | Named deposit detail timespan |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "batchDate": "string",
      "createdAt": "string",
      "id": "string",
      "transactionCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number | Deposit amount. |
| `batchDate` | string | Deposit batch date. |
| `createdAt` | string | Creation timestamp. |
| `id` | string | Stax deposit identifier. |
| `transactionCount` | number | Number of transactions included in the deposit. |

## Native endpoint

Through the native Stax API, this operation is `GET /query/depositDetail` (base URL `https://apiprod.fattlabs.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-deposit-details.md) for the provider-specific parameters and requirements.

