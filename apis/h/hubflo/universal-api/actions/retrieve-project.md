# Hubflo: Retrieve Project

Retrieves a project from Hubflo by ID.

```
GET https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/retrieve-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hubflo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/retrieve-project?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/retrieve-project?${params}`, {
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
| `id` | string | yes |  |

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

Through the native Hubflo API, this operation is `GET /projects/:id` (base URL `https://app.hubflo.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-project.md) for the provider-specific parameters and requirements.

