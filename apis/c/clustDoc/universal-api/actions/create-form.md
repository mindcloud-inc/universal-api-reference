# ClustDoc: Create Form



```
POST https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/create-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClustDoc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/create-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/create-form', {
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
| `title` | string | yes | Form title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "absolute_path": "string",
      "created_at": "string",
      "form_data": {},
      "id": 1,
      "is_live": true,
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
| `absolute_path` | string |  |
| `created_at` | string |  |
| `form_data` | object |  |
| `id` | number |  |
| `is_live` | boolean |  |
| `team_id` | number |  |
| `title` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native ClustDoc API, this operation is `POST /forms` (base URL `https://api.clustdoc.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-form.md) for the provider-specific parameters and requirements.

