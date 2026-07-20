# mfr Field Service Management: Update Service Request

Updates a service request in mfr Field Service Management.

```
PUT https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/update-service-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mfr Field Service Management `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/update-service-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "bodyId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/update-service-request', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "bodyId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes |  |
| `bodyId` | string | yes | Record ID in the request body. |
| `name` | string | no | Updated service request name. |
| `externalId` | string | no | Updated external identifier. |
| `customerId` | string | no | Customer company ID for the service request. |
| `description` | string | no | Updated service request description. |
| `state` | string | no | Updated service request state. |
| `type` | string | no | Updated service request type. |
| `targetTimeInMinutes` | number | no | Updated target duration in minutes. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native mfr Field Service Management API returns.

## Native endpoint

Through the native mfr Field Service Management API, this operation is `PUT ServiceRequests({{id}}L)` (base URL `https://portal.mobilefieldreport.com/odata`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-service-request.md) for the provider-specific parameters and requirements.

