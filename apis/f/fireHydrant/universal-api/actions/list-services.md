# FireHydrant: List Services

Retrieves services from FireHydrant.

```
GET https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/list-services
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FireHydrant `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/list-services?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/list-services?${params}`, {
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
| `impacted` | string | no | Filter by whether services are impacted by active incidents. |
| `name` | string | no | Search services by name. |
| `owner` | string | no | Filter by owning team ID. |
| `query` | string | no | Search services by name or description. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
      "pagination": {
        "count": 1,
        "items": 1,
        "last": 1,
        "page": 1,
        "pages": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].activeIncidents` | array<string> |  |
| `data[].alertOnAdd` | boolean |  |
| `data[].autoAddRespondingTeam` | boolean |  |
| `data[].checklists` | array<object> |  |
| `data[].completedChecks` | number |  |
| `data[].createdAt` | date |  |
| `data[].description` | string |  |
| `data[].environments` | array<object> |  |
| `data[].externalResources` | array<object> |  |
| `data[].functionalities` | array<object> |  |
| `data[].id` | string |  |
| `data[].labels` | object |  |
| `data[].lastImport` | object |  |
| `data[].links` | array<object> |  |
| `data[].managedBy` | object |  |
| `data[].managedBySettings` | object |  |
| `data[].name` | string |  |
| `data[].owner` | object |  |
| `data[].serviceChecklistUpdatedAt` | date |  |
| `data[].serviceTier` | number |  |
| `data[].slug` | string |  |
| `data[].teams` | array<object> |  |
| `data[].updatedAt` | date |  |
| `data[].updatedBy` | object |  |
| `pagination.count` | number |  |
| `pagination.items` | number |  |
| `pagination.last` | number |  |
| `pagination.page` | number |  |
| `pagination.pages` | number |  |

## Native endpoint

Through the native FireHydrant API, this operation is `GET /services` (base URL `https://api.firehydrant.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-services.md) for the provider-specific parameters and requirements.

