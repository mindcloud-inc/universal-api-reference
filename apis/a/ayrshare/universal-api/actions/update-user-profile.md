# Ayrshare: Update User Profile

Updates an existing user profile in Ayrshare.

```
PUT https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/update-user-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ayrshare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/update-user-profile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "profileKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/update-user-profile', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "profileKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `profileKey` | string | yes | Profile key for the user profile to update. |
| `title` | string | no | Updated profile title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "message": "string",
      "profileKey": "string",
      "refId": "string",
      "status": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | Ayrshare error code. |
| `message` | string | Update or error message. |
| `profileKey` | string | Profile key. |
| `refId` | string | Profile reference ID. |
| `status` | string | Update profile status. |
| `title` | string | Updated profile title. |

## Native endpoint

Through the native Ayrshare API, this operation is `PATCH /profiles` (base URL `https://api.ayrshare.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user-profile.md) for the provider-specific parameters and requirements.

