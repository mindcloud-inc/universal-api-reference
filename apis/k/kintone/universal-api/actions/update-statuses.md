# Kintone: Update Statuses

Updates record statuses in Kintone.

```
PUT https://connect.mindcloud.co/v1/universal/kintone/latest/actions/update-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kintone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kintone/latest/actions/update-statuses" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": 1,
  "records": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kintone/latest/actions/update-statuses', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": 1,
    "records": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | number | yes | The Kintone app ID. |
| `records` | list<object> | yes | An array of status update objects. Each item can include id, action, assignee, and revision. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "records": [
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
| `records` | array<object> | The status update results for each submitted record. |

## Native endpoint

Through the native Kintone API, this operation is `PUT /records/status.json` (base URL `{{credentials.baseUrl}}/k/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-statuses.md) for the provider-specific parameters and requirements.

