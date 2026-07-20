# BSC Designer: Set Indicator Info



```
PUT https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/set-indicator-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BSC Designer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/set-indicator-info" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "docId": "string",
  "guid": "string",
  "name": "Ava Chen",
  "indicatorType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/set-indicator-info', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "docId": "string",
    "guid": "string",
    "name": "Ava Chen",
    "indicatorType": "string"
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
| `name` | string | yes | Updated indicator name. |
| `description` | string | no | Updated indicator description. |
| `indicatorType` | string | yes | Indicator type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acceptValueData": true,
      "description": "string",
      "guid": "string",
      "indicatorType": "string",
      "initiatives": [
        {}
      ],
      "items": [
        {}
      ],
      "measure": "string",
      "measureNames": [
        "Ava Chen"
      ],
      "name": "Ava Chen",
      "updateInterval": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acceptValueData` | boolean |  |
| `description` | string |  |
| `guid` | string |  |
| `indicatorType` | string |  |
| `initiatives` | array<object> |  |
| `items` | array<object> |  |
| `measure` | string |  |
| `measureNames` | array<string> |  |
| `name` | string |  |
| `updateInterval` | string |  |

## Native endpoint

Through the native BSC Designer API, this operation is `PUT /rest/api/document/:docId/kpi/:guid` (base URL `https://www.webbsc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-indicator-info.md) for the provider-specific parameters and requirements.

