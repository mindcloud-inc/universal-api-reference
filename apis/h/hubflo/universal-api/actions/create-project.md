# Hubflo: Create Project

Creates a new project in Hubflo.

```
POST https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hubflo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `estimatedRevenueAmount` | number | no |  |
| `startDate` | string | no |  |
| `endDate` | string | no |  |
| `ownerId` | string | no |  |
| `ownerEmail` | string | no |  |
| `stageId` | string | no |  |
| `primaryContactId` | string | no |  |
| `address` | string | no |  |
| `workspaceId` | string | no |  |
| `tags` | list<string> | no |  |
| `userIds` | list<string> | no |  |

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

Through the native Hubflo API, this operation is `POST /projects` (base URL `https://app.hubflo.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

