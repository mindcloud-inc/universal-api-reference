# FireHydrant: List Teams

Retrieves teams from FireHydrant.

```
GET https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/list-teams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FireHydrant `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/list-teams?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/list-teams?${params}`, {
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
| `name` | string | no | Filter teams by name. |
| `query` | string | no | Search teams by name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "createdBy": {},
          "defaultSignalsEscalationPolicy": {},
          "description": "string",
          "functionalities": [
            {}
          ],
          "id": "string",
          "inSupportHours": true,
          "memberships": [
            {}
          ],
          "msTeamsChannel": {},
          "name": "Ava Chen",
          "ownedServices": [
            {}
          ],
          "respondingServices": [
            {}
          ],
          "restrictSignalsResourceManagement": true,
          "services": [
            {}
          ],
          "signalsIcalUrl": "https://example.com",
          "slackChannel": {},
          "slug": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
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
| `data[].createdBy` | object |  |
| `data[].defaultSignalsEscalationPolicy` | object |  |
| `data[].description` | string |  |
| `data[].functionalities` | array<object> |  |
| `data[].id` | string |  |
| `data[].inSupportHours` | boolean |  |
| `data[].memberships` | array<object> |  |
| `data[].msTeamsChannel` | object |  |
| `data[].name` | string |  |
| `data[].ownedServices` | array<object> |  |
| `data[].respondingServices` | array<object> |  |
| `data[].restrictSignalsResourceManagement` | boolean |  |
| `data[].services` | array<object> |  |
| `data[].signalsIcalUrl` | string |  |
| `data[].slackChannel` | object |  |
| `data[].slug` | string |  |
| `data[].updatedAt` | date |  |
| `pagination.count` | number |  |
| `pagination.items` | number |  |
| `pagination.last` | number |  |
| `pagination.page` | number |  |
| `pagination.pages` | number |  |

## Native endpoint

Through the native FireHydrant API, this operation is `GET /teams` (base URL `https://api.firehydrant.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-teams.md) for the provider-specific parameters and requirements.

