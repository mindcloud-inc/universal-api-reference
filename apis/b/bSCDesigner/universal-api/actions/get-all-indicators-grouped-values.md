# BSC Designer: Get All Indicators Grouped Values



```
GET https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/get-all-indicators-grouped-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BSC Designer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/get-all-indicators-grouped-values?connectionId=$CONNECTION_ID&docId=string&period=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "docId": "string",
  "period": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/get-all-indicators-grouped-values?${params}`, {
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
| `period` | string | yes | Grouping period: DAY, WEEK, MONTH, QUARTER, HALF_YEAR, or YEAR. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "end": "string",
      "items": [
        {}
      ],
      "period": "string",
      "start": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `end` | string | End of the grouped interval. |
| `items` | array<object> | Grouped values for all indicators. |
| `period` | string | Grouping period. |
| `start` | string | Start of the grouped interval. |

## Native endpoint

Through the native BSC Designer API, this operation is `GET /rest/api/document/:docId/kpi/indicatos/grouped-value/:period` (base URL `https://www.webbsc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-indicators-grouped-values.md) for the provider-specific parameters and requirements.

