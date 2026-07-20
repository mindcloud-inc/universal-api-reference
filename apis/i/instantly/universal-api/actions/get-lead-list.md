# Instantly: Get Lead List

Retrieves a lead list from Instantly.

```
GET https://connect.mindcloud.co/v1/universal/instantly/latest/actions/get-lead-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instantly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instantly/latest/actions/get-lead-list?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instantly/latest/actions/get-lead-list?${params}`, {
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
| `id` | string | yes | Lead list ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "has_enrichment_task": true,
      "id": "string",
      "name": "Ava Chen",
      "organization_id": "string",
      "owned_by": "string",
      "timestamp_created": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `has_enrichment_task` | boolean |  |
| `id` | string |  |
| `name` | string |  |
| `organization_id` | string |  |
| `owned_by` | string |  |
| `timestamp_created` | date |  |

## Native endpoint

Through the native Instantly API, this operation is `GET /api/v2/lead-lists/:id` (base URL `https://api.instantly.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lead-list.md) for the provider-specific parameters and requirements.

