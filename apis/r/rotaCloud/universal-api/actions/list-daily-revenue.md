# RotaCloud: List Daily Revenue



```
GET https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-daily-revenue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-daily-revenue?connectionId=$CONNECTION_ID&end=string&start=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "end": "string",
  "start": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-daily-revenue?${params}`, {
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
| `end` | string | yes |  |
| `locations` | number | no | Accepts multiple values in one string, delimited by `,`. |
| `start` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "string",
      "labour_percentage": 1,
      "location": 1,
      "revenue_actual": 1,
      "revenue_target": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | string |  |
| `labour_percentage` | number |  |
| `location` | number |  |
| `revenue_actual` | number |  |
| `revenue_target` | number |  |

## Native endpoint

Through the native RotaCloud API, this operation is `GET /v1/daily_revenue` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-daily-revenue.md) for the provider-specific parameters and requirements.

