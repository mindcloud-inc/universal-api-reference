# Gupshup: Update Business Profile Photo

Updates the business profile photo in Gupshup.

```
PUT https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/update-business-profile-photo
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gupshup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/update-business-profile-photo" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "string",
  "photo": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/update-business-profile-photo', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "string",
    "photo": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | string | yes | Gupshup app ID. |
| `photo` | file | yes | Business profile photo file or media value accepted by Gupshup. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Gupshup response message. |
| `status` | string | Update status returned by Gupshup. |

## Native endpoint

Through the native Gupshup API, this operation is `PUT /wa/app/{appId}/business/profile/photo` (base URL `https://api.gupshup.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-business-profile-photo.md) for the provider-specific parameters and requirements.

