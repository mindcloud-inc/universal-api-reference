# Famulor AI - Voice Agent: Update Mid Call Tool

Updates an existing mid-call tool in Famulor.

```
PUT https://connect.mindcloud.co/v1/universal/famulorAIVoiceAgent/latest/actions/update-mid-call-tool
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Famulor AI - Voice Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/famulorAIVoiceAgent/latest/actions/update-mid-call-tool" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/famulorAIVoiceAgent/latest/actions/update-mid-call-tool', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Explanation of when and how the assistant should use the tool. |
| `endpoint` | string | no | External API endpoint URL for the tool. |
| `id` | number | yes | Famulor mid-call tool ID. |
| `method` | string | no | HTTP method the tool should use. |
| `name` | string | no | Mid-call tool identifier. |

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
| `data` | object | Updated mid-call tool details. |
| `message` | string | Result message. |

## Native endpoint

Through the native Famulor AI - Voice Agent API, this operation is `PUT /user/tools/:id` (base URL `https://app.famulor.de/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-mid-call-tool.md) for the provider-specific parameters and requirements.

