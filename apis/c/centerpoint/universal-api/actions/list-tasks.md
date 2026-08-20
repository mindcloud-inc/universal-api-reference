# Centerpoint: List Tasks



```
GET https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-tasks?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields[tasks]` | string | no | Fields: fromCompany, fromProfile, toCompany |
| `fields[companies]` | string | no |  |
| `fields[properties]` | string | no |  |
| `fields[productions]` | string | no |  |
| `include` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "completedAt": "string",
        "completeNotes": {},
        "createdAt": "string",
        "creatorId": {},
        "deletedAt": {},
        "description": {},
        "dueDate": "string",
        "duration": {},
        "endDate": {},
        "event": "string",
        "fromCompanyId": 1,
        "fromProfileId": 1,
        "productionId": {},
        "propertyId": 1,
        "taskTypeId": 1,
        "title": "string",
        "toCompanyId": 1,
        "toProfileId": {},
        "updatedAt": "string"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.completedAt` | string |  |
| `attributes.completeNotes` | object |  |
| `attributes.createdAt` | string |  |
| `attributes.creatorId` | object |  |
| `attributes.deletedAt` | object |  |
| `attributes.description` | object |  |
| `attributes.dueDate` | string |  |
| `attributes.duration` | object |  |
| `attributes.endDate` | object |  |
| `attributes.event` | string |  |
| `attributes.fromCompanyId` | number |  |
| `attributes.fromProfileId` | number |  |
| `attributes.productionId` | object |  |
| `attributes.propertyId` | number |  |
| `attributes.taskTypeId` | number |  |
| `attributes.title` | string |  |
| `attributes.toCompanyId` | number |  |
| `attributes.toProfileId` | object |  |
| `attributes.updatedAt` | string |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Centerpoint API, this operation is `GET tasks` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

