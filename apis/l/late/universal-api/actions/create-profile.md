# Late: Create Profile



```
POST https://connect.mindcloud.co/v1/universal/late/latest/actions/create-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Late `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/late/latest/actions/create-profile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/late/latest/actions/create-profile', {
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
| `name` | string | yes |  |
| `description` | string | no |  |
| `color` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "profile": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider success message. |
| `profile` | object | Created profile payload. |

## Native endpoint

Through the native Late API, this operation is `POST /profiles` (base URL `https://zernio.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-profile.md) for the provider-specific parameters and requirements.

