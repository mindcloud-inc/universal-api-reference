# BSC Designer: Set Indicator Values



```
PUT https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/set-indicator-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BSC Designer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/set-indicator-values" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "docId": "string",
  "guid": "string",
  "date": "string",
  "value": 1,
  "target": 1,
  "baseline": 1,
  "min": 1,
  "max": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/set-indicator-values', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "docId": "string",
    "guid": "string",
    "date": "string",
    "value": 1,
    "target": 1,
    "baseline": 1,
    "min": 1,
    "max": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `docId` | string | yes | Document id or alias containing the indicator. |
| `guid` | string | yes | Indicator guid to update. |
| `date` | string | yes | Date in yyyy-MM-dd format. |
| `value` | number | yes | Indicator value at the given date. |
| `target` | number | yes | Target at the given date. |
| `baseline` | number | yes | Baseline at the given date. |
| `min` | number | yes | Minimum at the given date. |
| `max` | number | yes | Maximum at the given date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "baseline": 1,
      "baselineDate": "string",
      "date": "string",
      "item": {},
      "max": 1,
      "maxDate": "string",
      "min": 1,
      "minDate": "string",
      "target": 1,
      "targetDate": "string",
      "value": 1,
      "valueDate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseline` | number |  |
| `baselineDate` | string |  |
| `date` | string |  |
| `item` | object |  |
| `max` | number |  |
| `maxDate` | string |  |
| `min` | number |  |
| `minDate` | string |  |
| `target` | number |  |
| `targetDate` | string |  |
| `value` | number |  |
| `valueDate` | string |  |

## Native endpoint

Through the native BSC Designer API, this operation is `POST /rest/api/document/:docId/kpi/indicator/:guid/value/:date` (base URL `https://www.webbsc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-indicator-values.md) for the provider-specific parameters and requirements.

