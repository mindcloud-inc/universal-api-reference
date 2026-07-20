# BSC Designer: Get Indicator Value



```
GET https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/get-indicator-value
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BSC Designer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/get-indicator-value?connectionId=$CONNECTION_ID&docId=string&guid=string&date=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "docId": "string",
  "guid": "string",
  "date": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/get-indicator-value?${params}`, {
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
| `docId` | string | yes | Document ID or alias. |
| `guid` | string | yes | Indicator GUID. |
| `date` | string | yes | Date in yyyy-MM-dd format. |

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
| `baseline` | number | Baseline value. |
| `baselineDate` | string | Date for the baseline value. |
| `date` | string | Requested date. |
| `item` | object | Indicator metadata. |
| `max` | number | Maximum threshold. |
| `maxDate` | string | Date for the maximum threshold. |
| `min` | number | Minimum threshold. |
| `minDate` | string | Date for the minimum threshold. |
| `target` | number | Target value. |
| `targetDate` | string | Date for the target value. |
| `value` | number | Indicator value. |
| `valueDate` | string | Date for the indicator value. |

## Native endpoint

Through the native BSC Designer API, this operation is `GET /rest/api/document/:docId/kpi/indicator/:guid/value/:date` (base URL `https://www.webbsc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-indicator-value.md) for the provider-specific parameters and requirements.

