# Promptmate.io: Use Template



```
POST https://connect.mindcloud.co/v1/universal/promptmateio/latest/actions/use-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Promptmate.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/promptmateio/latest/actions/use-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/promptmateio/latest/actions/use-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes | The Promptmate template ID to use. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appId": "string",
      "message": "string",
      "templateId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appId` | string | Created Promptmate app ID. |
| `message` | string | Provider success message. |
| `templateId` | string | Template ID used to create the app. |

## Native endpoint

Through the native Promptmate.io API, this operation is `POST /templates/use` (base URL `https://api.promptmate.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/use-template.md) for the provider-specific parameters and requirements.

