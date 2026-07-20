# Matomo: ScheduledReports add Report



```
POST https://connect.mindcloud.co/v1/universal/matomo/latest/actions/scheduled-reports-add-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Matomo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/matomo/latest/actions/scheduled-reports-add-report" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "idSite": "1",
  "description": "string",
  "period": "day",
  "hour": "string",
  "reportType": "string",
  "reportFormat": "string",
  "reports": "string",
  "parameters": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/matomo/latest/actions/scheduled-reports-add-report', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "idSite": "1",
    "description": "string",
    "period": "day",
    "hour": "string",
    "reportType": "string",
    "reportFormat": "string",
    "reports": "string",
    "parameters": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `idSite` | number | yes | Matomo API parameter. Default: `1`. |
| `description` | string | yes | Matomo API parameter. |
| `period` | string | yes | Matomo API parameter. Default: `day`. |
| `hour` | string | yes | Matomo API parameter. |
| `reportType` | string | yes | Matomo API parameter. |
| `reportFormat` | string | yes | Matomo API parameter. |
| `reports` | string | yes | Matomo API parameter. |
| `parameters` | string | yes | Matomo API parameter. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `idSegment` | string | no | Matomo API parameter. |
| `evolutionPeriodFor` | string | no | Matomo API parameter. Default: `prev`. |
| `evolutionPeriodN` | string | no | Matomo API parameter. |
| `periodParam` | string | no | Matomo API parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "label": "string",
      "nb_actions": 1,
      "nb_visits": 1,
      "result": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `label` | string | Matomo response label |
| `nb_actions` | number | Actions |
| `nb_visits` | number | Visits |
| `result` | string | Operation result |
| `value` | string | Matomo response value |

## Native endpoint

Through the native Matomo API, this operation is `POST /index.php` (base URL `https://mindcloud.matomo.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scheduled-reports-add-report.md) for the provider-specific parameters and requirements.

