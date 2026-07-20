# 4HSE: List Incidents

Retrieves incidents from 4HSE.

```
GET https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-incidents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 4HSE `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-incidents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-incidents?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "code": "string",
      "dateIncident": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "officeIncidentId": "string",
      "officeName": "Ava Chen",
      "permission": "string",
      "status": "string",
      "subtenantId": "string",
      "tenantId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string | Incident category |
| `code` | string | Incident code |
| `dateIncident` | date | Incident date |
| `name` | string | Incident name |
| `officeIncidentId` | string | Incident identifier |
| `officeName` | string | Office name |
| `permission` | string | Permission level |
| `status` | string | Incident status |
| `subtenantId` | string | Office identifier |
| `tenantId` | string | Project identifier |

## Native endpoint

Through the native 4HSE API, this operation is `POST /v2/incident/index` (base URL `https://service.4hse.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-incidents.md) for the provider-specific parameters and requirements.

