# Chatling: Update Settings

Updates project settings in Chatling.

```
PUT https://connect.mindcloud.co/v1/universal/chatling/latest/actions/update-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatling/latest/actions/update-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "My Project"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatling/latest/actions/update-settings', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "My Project"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The project name. Example: `My Project`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "projectId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string | The name of the project. |
| `projectId` | string | The unique identifier of the project. |

## Native endpoint

Through the native Chatling API, this operation is `PATCH /project/settings` (base URL `https://api.chatling.ai/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-settings.md) for the provider-specific parameters and requirements.

