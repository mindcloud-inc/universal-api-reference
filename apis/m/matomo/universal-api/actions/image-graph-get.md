# Matomo: ImageGraph get



```
GET https://connect.mindcloud.co/v1/universal/matomo/latest/actions/image-graph-get
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Matomo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/matomo/latest/actions/image-graph-get?connectionId=$CONNECTION_ID&idSite=1&period=day&date=yesterday&apiModule=string&apiAction=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idSite": "1",
  "period": "day",
  "date": "yesterday",
  "apiModule": "string",
  "apiAction": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/matomo/latest/actions/image-graph-get?${params}`, {
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
| `apiModule` | string | yes | Matomo API parameter. |
| `apiAction` | string | yes | Matomo API parameter. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `graphType` | string | no | Matomo API parameter. |
| `outputType` | string | no | Matomo API parameter. Default: `0`. |
| `columns` | string | no | Matomo API parameter. |
| `labels` | string | no | Matomo API parameter. |
| `showLegend` | boolean | no | Matomo API parameter. Default: `1`. |
| `width` | string | no | Matomo API parameter. |
| `height` | string | no | Matomo API parameter. |
| `fontSize` | string | no | Matomo API parameter. Default: `9`. |
| `legendFontSize` | string | no | Matomo API parameter. |
| `aliasedGraph` | string | no | Matomo API parameter. Default: `1`. |
| `idGoal` | number | no | Matomo API parameter. |
| `colors` | string | no | Matomo API parameter. |
| `textColor` | string | no | Matomo API parameter. Default: `222222`. |
| `backgroundColor` | string | no | Matomo API parameter. Default: `FFFFFF`. |
| `gridColor` | string | no | Matomo API parameter. Default: `CCCCCC`. |
| `idSubtable` | number | no | Matomo API parameter. |
| `legendAppendMetric` | string | no | Matomo API parameter. Default: `1`. |
| `segment` | string | no | Matomo API parameter. |
| `idDimension` | string | no | Matomo API parameter. |

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

Through the native Matomo API, this operation is `POST /index.php` (base URL `https://mindcloud.matomo.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/image-graph-get.md) for the provider-specific parameters and requirements.

