# FireHydrant: Get Service

Retrieves a service from FireHydrant.

```
GET https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/get-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FireHydrant `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/get-service?connectionId=$CONNECTION_ID&serviceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "serviceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/get-service?${params}`, {
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
| `serviceId` | string | yes | The FireHydrant service ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeIncidents": [
        "string"
      ],
      "alertOnAdd": true,
      "autoAddRespondingTeam": true,
      "checklists": [
        {}
      ],
      "completedChecks": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "environments": [
        {}
      ],
      "externalResources": [
        {}
      ],
      "functionalities": [
        {}
      ],
      "id": "string",
      "labels": {},
      "lastImport": {},
      "links": [
        {}
      ],
      "managedBy": {},
      "managedBySettings": {},
      "name": "Ava Chen",
      "owner": {},
      "serviceChecklistUpdatedAt": "2026-05-07T12:00:00.000Z",
      "serviceTier": 1,
      "slug": "string",
      "teams": [
        {}
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedBy": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeIncidents` | array<string> |  |
| `alertOnAdd` | boolean |  |
| `autoAddRespondingTeam` | boolean |  |
| `checklists` | array<object> |  |
| `completedChecks` | number |  |
| `createdAt` | date |  |
| `description` | string |  |
| `environments` | array<object> |  |
| `externalResources` | array<object> |  |
| `functionalities` | array<object> |  |
| `id` | string |  |
| `labels` | object |  |
| `lastImport` | object |  |
| `links` | array<object> |  |
| `managedBy` | object |  |
| `managedBySettings` | object |  |
| `name` | string |  |
| `owner` | object |  |
| `serviceChecklistUpdatedAt` | date |  |
| `serviceTier` | number |  |
| `slug` | string |  |
| `teams` | array<object> |  |
| `updatedAt` | date |  |
| `updatedBy` | object |  |

## Native endpoint

Through the native FireHydrant API, this operation is `GET /services/:service_id` (base URL `https://api.firehydrant.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-service.md) for the provider-specific parameters and requirements.

