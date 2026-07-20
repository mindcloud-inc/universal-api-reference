# Matomo: Insights get Insights



```
GET https://connect.mindcloud.co/v1/universal/matomo/latest/actions/insights-get-insights
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Matomo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/matomo/latest/actions/insights-get-insights?connectionId=$CONNECTION_ID&idSite=1&period=day&date=yesterday&reportUniqueId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idSite": "1",
  "period": "day",
  "date": "yesterday",
  "reportUniqueId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/matomo/latest/actions/insights-get-insights?${params}`, {
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
| `idSite` | number | yes | Matomo API parameter. Default: `1`. |
| `period` | string | yes | Matomo API parameter. Default: `day`. |
| `date` | string | yes | Matomo API parameter. Default: `yesterday`. |
| `reportUniqueId` | string | yes | Matomo API parameter. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `segment` | string | no | Matomo API parameter. |
| `limitIncreaser` | string | no | Matomo API parameter. Default: `5`. |
| `limitDecreaser` | string | no | Matomo API parameter. Default: `5`. |
| `filterBy` | string | no | Matomo API parameter. |
| `minImpactPercent` | string | no | Matomo API parameter. Default: `2`. |
| `minGrowthPercent` | string | no | Matomo API parameter. Default: `20`. |
| `comparedToXPeriods` | string | no | Matomo API parameter. Default: `1`. |
| `orderBy` | string | no | Matomo API parameter. Default: `absolute`. |

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

Through the native Matomo API, this operation is `POST /index.php` (base URL `https://mindcloud.matomo.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/insights-get-insights.md) for the provider-specific parameters and requirements.

