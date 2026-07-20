# Colossyan: Create Avatar

Creates a new avatar in Colossyan.

```
POST https://connect.mindcloud.co/v1/universal/colossyan/latest/actions/create-avatar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Colossyan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/colossyan/latest/actions/create-avatar" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "displayName": "Ava Chen",
  "sourceFileUrl": "https://example.com",
  "gender": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/colossyan/latest/actions/create-avatar', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "displayName": "Ava Chen",
    "sourceFileUrl": "https://example.com",
    "gender": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `displayName` | string | yes | Name to display for the new avatar. |
| `sourceFileUrl` | string | yes | Public image or video URL used to generate the avatar. |
| `gender` | string | yes | Gender label for the new avatar. One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string | Identifier returned by Colossyan for the created avatar. |

## Native endpoint

Through the native Colossyan API, this operation is `POST /assets/actors` (base URL `https://app.colossyan.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-avatar.md) for the provider-specific parameters and requirements.

