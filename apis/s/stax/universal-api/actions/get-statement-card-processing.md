# Stax: Get Statement Card Processing

Retrieves statement card processing totals from Stax.

```
GET https://connect.mindcloud.co/v1/universal/stax/latest/actions/get-statement-card-processing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stax/latest/actions/get-statement-card-processing?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stax/latest/actions/get-statement-card-processing?${params}`, {
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
      "cardBrand": "string",
      "count": 1,
      "date": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number | Processed card volume for the row. |
| `cardBrand` | string | Card brand when the report is grouped by brand. |
| `count` | number | Number of processed card transactions for the row. |
| `date` | string | Statement date represented by the row. |

## Native endpoint

Through the native Stax API, this operation is `GET /query/statement/v3/volumes/card-processing` (base URL `https://apiprod.fattlabs.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-statement-card-processing.md) for the provider-specific parameters and requirements.

