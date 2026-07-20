# Hubflo: List Projects

Retrieves all project records from Hubflo.

```
GET https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hubflo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/list-projects?${params}`, {
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
| `page` | number | no |  |
| `perPage` | number | no |  |
| `ownerId` | string | no |  |
| `ownerEmail` | string | no |  |
| `contactId` | string | no |  |
| `contactEmail` | string | no |  |
| `contactPhone` | string | no |  |
| `workspaceId` | string | no |  |
| `name` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "city": "string",
      "country": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "end_date": "string",
      "estimated_revenue_amount": 1,
      "id": "string",
      "latitude": "string",
      "longitude": "string",
      "name": "Ava Chen",
      "owner_id": "string",
      "postal_code": "string",
      "primary_contact_full_name": "Ava Chen",
      "primary_contact_id": "string",
      "stage_id": "string",
      "stage_name": "Ava Chen",
      "start_date": "string",
      "state": "string",
      "tags": [
        "string"
      ],
      "workspace_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `city` | string |  |
| `country` | string |  |
| `created_at` | date |  |
| `end_date` | string |  |
| `estimated_revenue_amount` | number |  |
| `id` | string |  |
| `latitude` | string |  |
| `longitude` | string |  |
| `name` | string |  |
| `owner_id` | string |  |
| `postal_code` | string |  |
| `primary_contact_full_name` | string |  |
| `primary_contact_id` | string |  |
| `stage_id` | string |  |
| `stage_name` | string |  |
| `start_date` | string |  |
| `state` | string |  |
| `tags` | array<string> |  |
| `workspace_id` | string |  |

## Native endpoint

Through the native Hubflo API, this operation is `GET /projects` (base URL `https://app.hubflo.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

