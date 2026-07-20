# Sharetribe: Update User Profile

Updates an existing user profile in Sharetribe.

```
PUT https://connect.mindcloud.co/v1/universal/sharetribe/latest/actions/update-user-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sharetribe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sharetribe/latest/actions/update-user-profile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sharetribe/latest/actions/update-user-profile', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The ID of the user that is being updated. |
| `firstName` | string | no | User's first name. |
| `lastName` | string | no | User's last name. |
| `displayName` | string | no | User's chosen display name. |
| `bio` | string | no | User's bio text. |
| `publicData` | object | no | User public extended data object. |
| `protectedData` | object | no | User protected extended data object. |
| `privateData` | object | no | User private extended data object. |
| `metadata` | object | no | User public metadata object. |
| `profileImageId` | string | no | Previously uploaded image ID to set as the user's profile image. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "id": "string",
      "relationships": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object | Resource attributes payload. |
| `id` | string | Resource ID. |
| `relationships` | object | Resource relationships payload. |
| `type` | string | Resource type. |

## Native endpoint

Through the native Sharetribe API, this operation is `POST users/update_profile` (base URL `https://flex-integ-api.sharetribe.com/v1/integration_api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user-profile.md) for the provider-specific parameters and requirements.

