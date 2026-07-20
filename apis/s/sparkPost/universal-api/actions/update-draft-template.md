# SparkPost: Update Draft Template



```
PUT https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/update-draft-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SparkPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/update-draft-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/update-draft-template', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `html` | string | no | Updated HTML body for the draft. |
| `id` | string | yes | Template identifier. |
| `name` | string | no | Updated template name. |
| `subject` | string | no | Updated message subject. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": {},
      "description": "string",
      "hasDraft": true,
      "hasPublished": true,
      "id": "string",
      "lastUpdateTime": "string",
      "name": "Ava Chen",
      "options": {},
      "published": true,
      "sharedWithSubaccounts": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | object |  |
| `description` | string |  |
| `hasDraft` | boolean |  |
| `hasPublished` | boolean |  |
| `id` | string |  |
| `lastUpdateTime` | string |  |
| `name` | string |  |
| `options` | object |  |
| `published` | boolean |  |
| `sharedWithSubaccounts` | boolean |  |

## Native endpoint

Through the native SparkPost API, this operation is `PUT /templates/:id` (base URL `https://api.sparkpost.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-draft-template.md) for the provider-specific parameters and requirements.

