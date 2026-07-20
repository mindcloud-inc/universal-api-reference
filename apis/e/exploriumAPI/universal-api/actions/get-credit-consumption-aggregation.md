# Explorium: Get Credit Consumption Aggregation

Retrieves credit consumption aggregation from Explorium API.

```
GET https://connect.mindcloud.co/v1/universal/exploriumAPI/latest/actions/get-credit-consumption-aggregation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Explorium `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/exploriumAPI/latest/actions/get-credit-consumption-aggregation?connectionId=$CONNECTION_ID&fromDate=string&toDate=string&mode=string&resolution=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fromDate": "string",
  "toDate": "string",
  "mode": "string",
  "resolution": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/exploriumAPI/latest/actions/get-credit-consumption-aggregation?${params}`, {
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
| `fromDate` | string | yes | Start date and time for the aggregation period in ISO 8601 format. |
| `timezone` | string | no | Timezone for aggregation boundaries. |
| `toDate` | string | yes | End date and time for the aggregation period in ISO 8601 format. |
| `mode` | string | yes | Aggregation mode. |
| `resolution` | string | yes | Aggregation resolution for timely mode. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aggregations": [
        {}
      ],
      "fromDate": "string",
      "mode": "string",
      "resolution": "string",
      "responseContext": {},
      "timezone": "string",
      "toDate": "string",
      "totalCredits": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aggregations` | array<object> | Aggregation buckets. |
| `fromDate` | string | Aggregation start date. |
| `mode` | string | Aggregation mode. |
| `resolution` | string | Aggregation resolution. |
| `responseContext` | object | Explorium response metadata. |
| `timezone` | string | Aggregation timezone. |
| `toDate` | string | Aggregation end date. |
| `totalCredits` | number | Total credits consumed in the range. |

## Native endpoint

Through the native Explorium API, this operation is `POST /v1/credits/aggregation` (base URL `https://api.explorium.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-credit-consumption-aggregation.md) for the provider-specific parameters and requirements.

