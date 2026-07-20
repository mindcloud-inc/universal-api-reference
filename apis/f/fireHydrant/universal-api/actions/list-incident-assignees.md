# FireHydrant: List Incident Assignees

Retrieves incident role assignments from FireHydrant.

```
GET https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/list-incident-assignees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FireHydrant `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/list-incident-assignees?connectionId=$CONNECTION_ID&incidentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "incidentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/list-incident-assignees?${params}`, {
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
| `incidentId` | string | yes | The FireHydrant incident ID. |
| `status` | string | no | Filter assignees by assignment status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "incidentRole": {},
          "status": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "user": {}
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
| `data[].createdAt` | date |  |
| `data[].id` | string |  |
| `data[].incidentRole` | object |  |
| `data[].status` | string |  |
| `data[].updatedAt` | date |  |
| `data[].user` | object |  |
| `pagination.count` | number |  |
| `pagination.items` | number |  |
| `pagination.last` | number |  |
| `pagination.page` | number |  |
| `pagination.pages` | number |  |

## Native endpoint

Through the native FireHydrant API, this operation is `GET /incidents/:incident_id/role_assignments` (base URL `https://api.firehydrant.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-incident-assignees.md) for the provider-specific parameters and requirements.

