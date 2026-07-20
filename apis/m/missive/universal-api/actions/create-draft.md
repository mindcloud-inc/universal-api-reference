# Missive: Create Draft

Creates a draft in your Missive workspace.

```
POST https://connect.mindcloud.co/v1/universal/missive/latest/actions/create-draft
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Missive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/missive/latest/actions/create-draft" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/missive/latest/actions/create-draft', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subject` | string | no | Draft subject. |
| `body` | string | no | Draft body as HTML or text. |
| `conversation` | string | no | Conversation ID to append the draft to an existing conversation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conversation": "string",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conversation` | string |  |
| `id` | string |  |

## Native endpoint

Through the native Missive API, this operation is `POST /drafts` (base URL `https://public.missiveapp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-draft.md) for the provider-specific parameters and requirements.

