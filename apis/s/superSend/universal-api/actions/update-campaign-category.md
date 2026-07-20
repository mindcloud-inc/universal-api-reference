# SuperSend: Update Campaign Category

Updates an existing campaign category in SuperSend.

```
PUT https://connect.mindcloud.co/v1/universal/superSend/latest/actions/update-campaign-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/update-campaign-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "string",
  "categoryId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superSend/latest/actions/update-campaign-category', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "string",
    "categoryId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | string | yes |  |
| `categoryId` | string | yes | Category ID to update |
| `name` | string | yes |  |

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

Through the native SuperSend API, this operation is `PATCH /campaign-categories` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-campaign-category.md) for the provider-specific parameters and requirements.

