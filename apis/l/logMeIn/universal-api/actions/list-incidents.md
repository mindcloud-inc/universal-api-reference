# LogMeIn: List Incidents

Retrieves a list of incidents from LogMeIn.

```
GET https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/list-incidents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LogMeIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/list-incidents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/list-incidents?${params}`, {
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
| `serviceId` | string | no | Service identifier. Leave blank for all services. |
| `keyword` | string | no | String to filter incidents. |
| `pageSize` | number | no | Number of incidents per page. |
| `pageNumber` | number | no | Page number to retrieve. |
| `sort` | string | no | Field to sort by. Prefix with '-' for descending order. |
| `createdAtFrom` | date | no | Filter incidents created from this date. |
| `createdAtTo` | date | no | Filter incidents created until this date. |
| `dueDateFrom` | date | no | Filter incidents due from this date. |
| `dueDateTo` | date | no | Filter incidents due until this date. |
| `updatedAtFrom` | date | no | Filter incidents updated from this date. |
| `updatedAtTo` | date | no | Filter incidents updated until this date. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assignedTo` | string | no | Assigned user IDs as a comma-separated list or repeated query parameter. |
| `requestedBy` | string | no | Requested-by user IDs as a comma-separated list or repeated query parameter. |
| `ticketType` | string | no | Ticket type filter. |
| `category` | string | no | Category names as a comma-separated list or repeated query parameter. |
| `priority` | string | no | Priority values as a comma-separated list or repeated query parameter. |
| `status` | string | no | Status names as a comma-separated list or repeated query parameter. |
| `tag` | string | no | Tag names as a comma-separated list or repeated query parameter. |
| `include` | string | no | Related entities to include as a comma-separated list or repeated query parameter. |
| `extraFields` | string | no | Extra fields to include as a comma-separated list or repeated query parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "priority": "string",
      "referenceNum": "string",
      "status": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `priority` | string |  |
| `referenceNum` | string |  |
| `status` | string |  |
| `title` | string |  |

## Native endpoint

Through the native LogMeIn API, this operation is `GET /goto-resolve-ticketing/v1/incidents` (base URL `https://api.goto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-incidents.md) for the provider-specific parameters and requirements.

