# SuperSend: Get Team Usage

Retrieves team usage from SuperSend.

```
GET https://connect.mindcloud.co/v1/universal/superSend/latest/actions/get-team-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/get-team-usage?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superSend/latest/actions/get-team-usage?${params}`, {
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
| `id` | string | yes | Resource ID (UUID) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contacts_limit": 1,
      "contacts_used": 1,
      "is_at_limit": true,
      "team_id": "string",
      "team_name": "Ava Chen",
      "usage_percentage": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contacts_limit` | number |  |
| `contacts_used` | number |  |
| `is_at_limit` | boolean |  |
| `team_id` | string |  |
| `team_name` | string |  |
| `usage_percentage` | number |  |

## Native endpoint

Through the native SuperSend API, this operation is `GET /teams/{id}/usage` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team-usage.md) for the provider-specific parameters and requirements.

