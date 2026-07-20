# BSC Designer: Balance Scorecard



```
PUT https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/balance-scorecard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BSC Designer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/balance-scorecard" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "docId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/balance-scorecard', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "docId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `docId` | string | yes | Document id or alias to balance. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "indicatorGuid": "string",
      "indicatorName": "Ava Chen",
      "newWeight": 1,
      "oldWeight": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `indicatorGuid` | string |  |
| `indicatorName` | string |  |
| `newWeight` | number |  |
| `oldWeight` | number |  |

## Native endpoint

Through the native BSC Designer API, this operation is `PUT /rest/api/document/:docId/kpi/weight-balance` (base URL `https://www.webbsc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/balance-scorecard.md) for the provider-specific parameters and requirements.

