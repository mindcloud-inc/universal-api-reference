# Tophhie Cloud: Get PDS Uptime Stats

Retrieves PDS uptime statistics from Tophhie Cloud.

```
GET https://connect.mindcloud.co/v1/universal/tophhieCloud/latest/actions/get-pds-uptime-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tophhie Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tophhieCloud/latest/actions/get-pds-uptime-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tophhieCloud/latest/actions/get-pds-uptime-stats?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `startDate` | date | no | Optional start date for uptime statistics. |
| `endDate` | date | no | Optional end date for uptime statistics. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availability": 1,
      "average_incident": 1,
      "longest_incident": 1,
      "number_of_incidents": 1,
      "total_downtime": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availability` | number | Availability percentage. |
| `average_incident` | number | Average incident duration. |
| `longest_incident` | number | Longest incident duration. |
| `number_of_incidents` | number | Number of incidents. |
| `total_downtime` | number | Total downtime. |

## Native endpoint

Through the native Tophhie Cloud API, this operation is `GET /pds/uptimeStats` (base URL `https://api.tophhie.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pds-uptime-stats.md) for the provider-specific parameters and requirements.

