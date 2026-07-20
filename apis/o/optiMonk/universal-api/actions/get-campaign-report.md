# OptiMonk: Get Campaign Report

Retrieves a campaign report from OptiMonk.

```
GET https://connect.mindcloud.co/v1/universal/optiMonk/latest/actions/get-campaign-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OptiMonk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/optiMonk/latest/actions/get-campaign-report?connectionId=$CONNECTION_ID&campaignId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/optiMonk/latest/actions/get-campaign-report?${params}`, {
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
| `campaignId` | number | yes | The OptiMonk campaign ID. |
| `groupBy` | string | no | Report grouping granularity. |
| `from` | string | no | Start date or datetime. |
| `to` | string | no | End date or datetime. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conversionRates": {},
      "conversions": {},
      "impressions": {},
      "period": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conversionRates` | object |  |
| `conversions` | object |  |
| `impressions` | object |  |
| `period` | object |  |

## Native endpoint

Through the native OptiMonk API, this operation is `GET /report/{campaignId}` (base URL `https://api.optimonk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-report.md) for the provider-specific parameters and requirements.

