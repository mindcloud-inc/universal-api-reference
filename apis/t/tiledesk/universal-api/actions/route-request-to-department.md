# Tiledesk: Route Request To Department

Routes a request to a department in Tiledesk.

```
PUT https://connect.mindcloud.co/v1/universal/tiledesk/latest/actions/route-request-to-department
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tiledesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tiledesk/latest/actions/route-request-to-department" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "requestId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tiledesk/latest/actions/route-request-to-department', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "requestId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `requestId` | string | yes | The request identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "departmentId": "string",
      "request_id": "string",
      "status": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `departmentId` | string |  |
| `request_id` | string |  |
| `status` | number |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Tiledesk API, this operation is `PUT /{{credentials.projectId}}/requests/:requestId/departments` (base URL `https://api.tiledesk.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/route-request-to-department.md) for the provider-specific parameters and requirements.

