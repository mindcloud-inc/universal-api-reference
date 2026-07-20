# Florm: Create Magic Link

Creates a login magic link in Florm.

```
POST https://connect.mindcloud.co/v1/universal/florm/latest/actions/create-magic-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Florm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/florm/latest/actions/create-magic-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/florm/latest/actions/create-magic-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Email address to receive the Florm magic link. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "guid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Email address that received the magic link. |
| `guid` | string | GUID of the created magic-link challenge. |

## Native endpoint

Through the native Florm API, this operation is `POST /v1/auth/magic-links` (base URL `https://api.florm.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-magic-link.md) for the provider-specific parameters and requirements.

