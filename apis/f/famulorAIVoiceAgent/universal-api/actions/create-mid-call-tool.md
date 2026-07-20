# Famulor AI - Voice Agent: Create Mid Call Tool

Creates a new mid-call tool in Famulor.

```
POST https://connect.mindcloud.co/v1/universal/famulorAIVoiceAgent/latest/actions/create-mid-call-tool
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Famulor AI - Voice Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/famulorAIVoiceAgent/latest/actions/create-mid-call-tool" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "description": "string",
  "endpoint": "string",
  "method": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/famulorAIVoiceAgent/latest/actions/create-mid-call-tool', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "description": "string",
    "endpoint": "string",
    "method": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | yes | Explanation of when and how the assistant should use the tool. |
| `endpoint` | string | yes | External API endpoint URL for the tool. |
| `method` | string | yes | HTTP method the tool should use. |
| `name` | string | yes | Mid-call tool identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Created mid-call tool details. |
| `message` | string | Result message. |

## Native endpoint

Through the native Famulor AI - Voice Agent API, this operation is `POST /user/tools` (base URL `https://app.famulor.de/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-mid-call-tool.md) for the provider-specific parameters and requirements.

