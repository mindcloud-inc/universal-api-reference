# Stax: Get Statement Fees

Retrieves statement fee details from Stax.

```
GET https://connect.mindcloud.co/v1/universal/stax/latest/actions/get-statement-fees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stax/latest/actions/get-statement-fees?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stax/latest/actions/get-statement-fees?${params}`, {
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
| `endDate` | string | no | Statement interval end date |
| `startDate` | string | no | Statement interval start date |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "count": 1,
      "date": "string",
      "feeType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number | Fee amount for the row. |
| `count` | number | Number of fee events in the row. |
| `date` | string | Statement date represented by the row. |
| `feeType` | string | Fee category when provided by Stax. |

## Native endpoint

Through the native Stax API, this operation is `GET /query/statement/v3/fees` (base URL `https://apiprod.fattlabs.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-statement-fees.md) for the provider-specific parameters and requirements.

