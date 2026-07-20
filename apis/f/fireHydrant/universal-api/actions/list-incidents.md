# FireHydrant: List Incidents

Retrieves incidents from FireHydrant.

```
GET https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/list-incidents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FireHydrant `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/list-incidents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/list-incidents?${params}`, {
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
| `query` | string | no | Search incident name, summary, and description. |
| `name` | string | no | Filter incidents by name. |
| `services` | string | no | Comma-separated service IDs to filter incidents by impacted services. Accepts multiple values in one string, delimited by `,`. |
| `teams` | string | no | Comma-separated team IDs to filter incidents by teams. Accepts multiple values in one string, delimited by `,`. |
| `severities` | string | no | Comma-separated severities to filter incidents. Accepts multiple values in one string, delimited by `,`. |
| `startDate` | date | no | Filter incidents that started on or after this timestamp. |
| `endDate` | date | no | Filter incidents that started on or before this timestamp. |
| `status` | string | no | Filter by incident status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "active": true,
          "createdAt": "2026-05-07T12:00:00.000Z",
          "createdBy": {},
          "currentMilestone": "string",
          "customerImpactSummary": "string",
          "customersImpacted": 1,
          "description": "string",
          "discardedAt": "2026-05-07T12:00:00.000Z",
          "environments": [
            {}
          ],
          "functionalities": [
            {}
          ],
          "id": "string",
          "impacts": [
            {}
          ],
          "incidentType": {},
          "incidentUrl": "https://example.com",
          "lastNote": {},
          "lastUpdate": "string",
          "name": "Ava Chen",
          "number": 1,
          "organizationId": "string",
          "priority": "string",
          "privateId": "string",
          "privateStatusPageUrl": "https://example.com",
          "services": [
            {}
          ],
          "severity": "string",
          "severityColor": "string",
          "startedAt": "2026-05-07T12:00:00.000Z",
          "summary": "string",
          "tagList": [
            "string"
          ]
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
| `data[].active` | boolean |  |
| `data[].createdAt` | date |  |
| `data[].createdBy` | object |  |
| `data[].currentMilestone` | string |  |
| `data[].customerImpactSummary` | string |  |
| `data[].customersImpacted` | number |  |
| `data[].description` | string |  |
| `data[].discardedAt` | date |  |
| `data[].environments` | array<object> |  |
| `data[].functionalities` | array<object> |  |
| `data[].id` | string |  |
| `data[].impacts` | array<object> |  |
| `data[].incidentType` | object |  |
| `data[].incidentUrl` | string |  |
| `data[].lastNote` | object |  |
| `data[].lastUpdate` | string |  |
| `data[].name` | string |  |
| `data[].number` | number |  |
| `data[].organizationId` | string |  |
| `data[].priority` | string |  |
| `data[].privateId` | string |  |
| `data[].privateStatusPageUrl` | string |  |
| `data[].services` | array<object> |  |
| `data[].severity` | string |  |
| `data[].severityColor` | string |  |
| `data[].startedAt` | date |  |
| `data[].summary` | string |  |
| `data[].tagList` | array<string> |  |
| `pagination.count` | number |  |
| `pagination.items` | number |  |
| `pagination.last` | number |  |
| `pagination.page` | number |  |
| `pagination.pages` | number |  |

## Native endpoint

Through the native FireHydrant API, this operation is `GET /incidents` (base URL `https://api.firehydrant.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-incidents.md) for the provider-specific parameters and requirements.

