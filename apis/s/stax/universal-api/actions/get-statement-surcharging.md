# Stax: Get Statement Surcharging

Retrieves statement surcharging totals from Stax.

```
GET https://connect.mindcloud.co/v1/universal/stax/latest/actions/get-statement-surcharging
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stax/latest/actions/get-statement-surcharging?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stax/latest/actions/get-statement-surcharging?${params}`, {
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
      "rate": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number | Total surcharge amount for the row. |
| `count` | number | Number of surcharged transactions in the row. |
| `date` | string | Statement date represented by the row. |
| `rate` | number | Applied surcharge rate when provided by Stax. |

## Native endpoint

Through the native Stax API, this operation is `GET /query/statement/v3/surcharges` (base URL `https://apiprod.fattlabs.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-statement-surcharging.md) for the provider-specific parameters and requirements.

