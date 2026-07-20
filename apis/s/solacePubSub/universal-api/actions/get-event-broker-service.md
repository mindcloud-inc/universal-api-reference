# Solace PubSub+: Get Event Broker Service

Retrieves an event broker service from Solace PubSub+.

```
GET https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-event-broker-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Solace PubSub+ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-event-broker-service?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-event-broker-service?${params}`, {
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
| `id` | string | yes | Event broker service identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adminState": {},
      "createdTime": "2026-05-07T12:00:00.000Z",
      "datacenterId": "string",
      "eventBrokerServiceVersion": "string",
      "eventMeshId": "string",
      "id": "string",
      "name": "Ava Chen",
      "ongoingOperationIds": [
        "string"
      ],
      "type": "string",
      "updatedTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adminState` | object |  |
| `createdTime` | date |  |
| `datacenterId` | string |  |
| `eventBrokerServiceVersion` | string |  |
| `eventMeshId` | string |  |
| `id` | string |  |
| `name` | string |  |
| `ongoingOperationIds` | array<string> |  |
| `type` | string |  |
| `updatedTime` | date |  |

## Native endpoint

Through the native Solace PubSub+ API, this operation is `GET /api/v2/missionControl/eventBrokerServices/{id}` (base URL `https://api.solace.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-broker-service.md) for the provider-specific parameters and requirements.

