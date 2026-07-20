# ClustDoc: Create Template



```
POST https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/create-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClustDoc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/create-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/create-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Template title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "background": 1,
      "category": "string",
      "collect_phone": true,
      "color": "string",
      "created_at": "string",
      "deadline_type": "string",
      "id": 1,
      "is_live": true,
      "language": "string",
      "signature": "string",
      "team_id": 1,
      "title": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `background` | number |  |
| `category` | string |  |
| `collect_phone` | boolean |  |
| `color` | string |  |
| `created_at` | string |  |
| `deadline_type` | string |  |
| `id` | number |  |
| `is_live` | boolean |  |
| `language` | string |  |
| `signature` | string |  |
| `team_id` | number |  |
| `title` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native ClustDoc API, this operation is `POST /templates` (base URL `https://api.clustdoc.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-template.md) for the provider-specific parameters and requirements.

