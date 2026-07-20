# Gupshup: Delete Business Profile Photo

Deletes the business profile photo from Gupshup.

```
DELETE https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/delete-business-profile-photo
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gupshup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/delete-business-profile-photo?connectionId=$CONNECTION_ID&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/delete-business-profile-photo?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | string | yes | Gupshup app ID. |

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
| `status` | string | Delete status returned by Gupshup. |

## Native endpoint

Through the native Gupshup API, this operation is `DELETE /wa/app/{appId}/business/profile/photo` (base URL `https://api.gupshup.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-business-profile-photo.md) for the provider-specific parameters and requirements.

