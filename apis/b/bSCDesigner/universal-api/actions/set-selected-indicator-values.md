# BSC Designer: Set Selected Indicator Values



```
PUT https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/set-selected-indicator-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BSC Designer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/set-selected-indicator-values" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "docId": "string",
  "date": "string",
  "values": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/set-selected-indicator-values', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "docId": "string",
    "date": "string",
    "values": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `docId` | string | yes | Document id or alias containing the indicators. |
| `date` | string | yes | Date in yyyy-MM-dd format. |
| `values` | list<object> | yes | Array of indicator value payloads shaped like the provider RestKpiSetValue model. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "values": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `values` | array<object> |  |

## Native endpoint

Through the native BSC Designer API, this operation is `POST /rest/api/document/:docId/kpi/batch/set-value/:date` (base URL `https://www.webbsc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-selected-indicator-values.md) for the provider-specific parameters and requirements.

