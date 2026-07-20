# Stax: Get Statement Refunds and Adjustments

Retrieves statement refunds and adjustments from Stax.

```
GET https://connect.mindcloud.co/v1/universal/stax/latest/actions/get-statement-refunds-and-adjustments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stax/latest/actions/get-statement-refunds-and-adjustments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stax/latest/actions/get-statement-refunds-and-adjustments?${params}`, {
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
| `endDate` | string | no | Report interval end date |
| `startDate` | string | no | Report interval start date |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "count": 1,
      "date": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number | Refund or adjustment amount for the row. |
| `count` | number | Number of refund or adjustment events in the row. |
| `date` | string | Statement date represented by the row. |
| `type` | string | Refund or adjustment type when provided by Stax. |

## Native endpoint

Through the native Stax API, this operation is `GET /query/statement/v3/adjustments` (base URL `https://apiprod.fattlabs.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-statement-refunds-and-adjustments.md) for the provider-specific parameters and requirements.

