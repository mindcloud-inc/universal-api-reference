# Userback: Create Feedback Screenshot

Creates a screenshot for a Userback feedback item.

```
POST https://connect.mindcloud.co/v1/universal/userback/latest/actions/create-feedback-screenshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Userback `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/userback/latest/actions/create-feedback-screenshot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "feedbackId": "7378423",
  "files": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/userback/latest/actions/create-feedback-screenshot', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "feedbackId": "7378423",
    "files": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `feedbackId` | number | yes | Parent feedback ID. Example: `7378423`. |
| `files` | file | yes | One or more screenshot files to upload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "string",
      "feedbackId": 1,
      "height": 1,
      "id": 1,
      "url": "https://example.com",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | string |  |
| `feedbackId` | number |  |
| `height` | number |  |
| `id` | number |  |
| `url` | string |  |
| `width` | number |  |

## Native endpoint

Through the native Userback API, this operation is `POST /feedback/screenshot` (base URL `https://rest.userback.io/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-feedback-screenshot.md) for the provider-specific parameters and requirements.

