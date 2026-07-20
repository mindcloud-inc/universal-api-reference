# E2B: Create Volume

Creates a new team volume in E2B.

```
POST https://connect.mindcloud.co/v1/universal/e2B/latest/actions/create-volume
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a E2B `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/e2B/latest/actions/create-volume" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/e2B/latest/actions/create-volume', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the volume. May contain letters, numbers, underscores, and hyphens. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "token": "string",
      "volumeID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string | Name of the volume. |
| `token` | string | Auth token for interacting with volume content. |
| `volumeID` | string | ID of the volume. |

## Native endpoint

Through the native E2B API, this operation is `POST /volumes` (base URL `https://api.e2b.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-volume.md) for the provider-specific parameters and requirements.

