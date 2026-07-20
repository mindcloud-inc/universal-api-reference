# SuperSend: List Campaign Categories

Retrieves campaign categories from SuperSend.

```
GET https://connect.mindcloud.co/v1/universal/superSend/latest/actions/list-campaign-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/list-campaign-categories?connectionId=$CONNECTION_ID&teamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superSend/latest/actions/list-campaign-categories?${params}`, {
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
| `teamId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign_count": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "org_id": "string",
      "team_id": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign_count` | number |  |
| `created_at` | date |  |
| `id` | string |  |
| `name` | string |  |
| `org_id` | string |  |
| `team_id` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native SuperSend API, this operation is `GET /campaign-categories` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaign-categories.md) for the provider-specific parameters and requirements.

