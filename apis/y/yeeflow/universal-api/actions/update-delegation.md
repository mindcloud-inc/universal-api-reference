# Yeeflow: Update Delegation



```
PUT https://connect.mindcloud.co/v1/universal/yeeflow/latest/actions/update-delegation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yeeflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/yeeflow/latest/actions/update-delegation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/yeeflow/latest/actions/update-delegation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no | Delegation ID from Yeeflow. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Data": "string",
      "Message": "string",
      "Status": 1,
      "TotalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Data` | string |  |
| `Message` | string |  |
| `Status` | number |  |
| `TotalCount` | number |  |

## Native endpoint

Through the native Yeeflow API, this operation is `PUT /workflow/delegates/:id` (base URL `https://api.yeeflow.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-delegation.md) for the provider-specific parameters and requirements.

