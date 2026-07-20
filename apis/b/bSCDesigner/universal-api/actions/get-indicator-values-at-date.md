# BSC Designer: Get Indicator Values At Date



```
GET https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/get-indicator-values-at-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BSC Designer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/get-indicator-values-at-date?connectionId=$CONNECTION_ID&documentId=string&indicatorGuid=string&date=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string",
  "indicatorGuid": "string",
  "date": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/get-indicator-values-at-date?${params}`, {
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
| `documentId` | string | yes | Document ID. |
| `indicatorGuid` | string | yes | Indicator GUID. |
| `date` | string | yes | Date in yyyy-MM-dd format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "baseline": 1,
      "max": 1,
      "min": 1,
      "score": 1,
      "target": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseline` | number | Baseline at the requested date. |
| `max` | number | Maximum threshold at the requested date. |
| `min` | number | Minimum threshold at the requested date. |
| `score` | number | Indicator score at the requested date. |
| `target` | number | Target at the requested date. |

## Native endpoint

Through the native BSC Designer API, this operation is `GET /rest/api/document/:documentId/kpi/indicator/:indicatorGuid/values/:date` (base URL `https://www.webbsc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-indicator-values-at-date.md) for the provider-specific parameters and requirements.

