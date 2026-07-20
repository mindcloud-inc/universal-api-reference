# CrowdPower: Get Events

Retrieves events from CrowdPower.

```
GET https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/get-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CrowdPower `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/get-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/get-events?${params}`, {
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
| `q` | string | no | Search query for events. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "color": "string",
      "created_at": 1,
      "deleted_at": 1,
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "project_id": "string",
      "properties": [
        {}
      ],
      "updated_at": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string |  |
| `color` | string |  |
| `created_at` | number |  |
| `deleted_at` | number |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `project_id` | string |  |
| `properties` | array<object> |  |
| `updated_at` | number |  |

## Native endpoint

Through the native CrowdPower API, this operation is `GET projects/{{credentials.projectId}}/events` (base URL `https://api.crowdpower.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-events.md) for the provider-specific parameters and requirements.

