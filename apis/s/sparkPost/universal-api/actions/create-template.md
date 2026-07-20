# SparkPost: Create Template



```
POST https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/create-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SparkPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/create-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fromEmail": "ava@example.com",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/create-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fromEmail": "ava@example.com",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fromEmail` | string | yes | Sender email address for the template draft. |
| `fromName` | string | no | Sender display name for the template draft. |
| `html` | string | no | HTML body for the template. |
| `id` | string | yes | Unique template identifier. |
| `name` | string | no | Human-readable template name. |
| `subject` | string | no | Default message subject. |
| `text` | string | no | Plain-text content for the template draft. |

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
| `published` | boolean |  |
| `sharedWithSubaccounts` | boolean |  |

## Native endpoint

Through the native SparkPost API, this operation is `POST /templates` (base URL `https://api.sparkpost.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-template.md) for the provider-specific parameters and requirements.

