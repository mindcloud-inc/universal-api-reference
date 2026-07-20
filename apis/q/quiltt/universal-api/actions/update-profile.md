# Quiltt: Update Profile



```
PUT https://connect.mindcloud.co/v1/universal/quiltt/latest/actions/update-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quiltt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/quiltt/latest/actions/update-profile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "profileId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quiltt/latest/actions/update-profile', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "profileId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | no | Updated profile email address. |
| `name` | string | no | Updated profile display name. |
| `phone` | string | no | Updated profile phone number. |
| `profileId` | string | yes | Quiltt profile ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "at": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dateOfBirth": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": "string",
      "metadata": {},
      "name": "Ava Chen",
      "names": {},
      "phone": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `at` | date |  |
| `createdAt` | date |  |
| `dateOfBirth` | date |  |
| `email` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `name` | string |  |
| `names` | object |  |
| `phone` | string |  |
| `updatedAt` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native Quiltt API, this operation is `PATCH /v1/profiles/:profileId` (base URL `https://api.quiltt.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-profile.md) for the provider-specific parameters and requirements.

