# Solace PubSub+: Get Service Operation

Retrieves a service operation from Solace PubSub+.

```
GET https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-service-operation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Solace PubSub+ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-service-operation?connectionId=$CONNECTION_ID&serviceId=string&operationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "serviceId": "string",
  "operationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-service-operation?${params}`, {
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
| `serviceId` | string | yes | Event broker service identifier. |
| `operationId` | string | yes | Service operation identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedTime": "2026-05-07T12:00:00.000Z",
      "createdTime": "2026-05-07T12:00:00.000Z",
      "error": {},
      "id": "string",
      "operationType": {},
      "progressLogs": [
        {}
      ],
      "resourceId": "string",
      "resourceType": "string",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedTime` | date |  |
| `createdTime` | date |  |
| `error` | object |  |
| `id` | string |  |
| `operationType` | object |  |
| `progressLogs` | array<object> |  |
| `resourceId` | string |  |
| `resourceType` | string |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Solace PubSub+ API, this operation is `GET /api/v2/missionControl/eventBrokerServices/{serviceId}/operations/{operationId}` (base URL `https://api.solace.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-service-operation.md) for the provider-specific parameters and requirements.

