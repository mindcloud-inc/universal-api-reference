# Umbler Talk: Create Quick Answer

Creates a new quick answer in Umbler Talk.

```
POST https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/create-quick-answer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umbler Talk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/create-quick-answer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "string",
  "name": "Ava Chen",
  "organizationId": "string",
  "visibility": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/create-quick-answer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "string",
    "name": "Ava Chen",
    "organizationId": "string",
    "visibility": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | yes | Quick answer content. |
| `name` | string | yes | Quick answer name. |
| `organizationId` | string | yes | The organization ID. |
| `visibility` | string | yes | Quick answer visibility. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_t": "string",
      "content": "string",
      "createdAtUTC": "2026-05-07T12:00:00.000Z",
      "groupIds": [
        "string"
      ],
      "id": "string",
      "name": "Ava Chen",
      "organizationMember": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_t` | string |  |
| `content` | string |  |
| `createdAtUTC` | date |  |
| `groupIds` | array<string> |  |
| `id` | string |  |
| `name` | string |  |
| `organizationMember` | object |  |

## Native endpoint

Through the native Umbler Talk API, this operation is `POST /v1/quick-answers/` (base URL `https://app-utalk.umbler.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-quick-answer.md) for the provider-specific parameters and requirements.

