# Pumble: List Users

Retrieves users from a Pumble workspace.

```
GET https://connect.mindcloud.co/v1/universal/pumble/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pumble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pumble/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pumble/latest/actions/list-users?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "activeUntil": 1,
      "automaticallyTimeZone": true,
      "avatar": {
        "fullPath": "string",
        "scaledPath": "string"
      },
      "email": "ava@example.com",
      "id": "string",
      "isAddonBot": true,
      "isPumbleBot": true,
      "name": "Ava Chen",
      "phone": "string",
      "role": "string",
      "status": "string",
      "timeZoneId": "string",
      "title": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeUntil` | number |  |
| `automaticallyTimeZone` | boolean |  |
| `avatar.fullPath` | string |  |
| `avatar.scaledPath` | string |  |
| `email` | string |  |
| `id` | string |  |
| `isAddonBot` | boolean |  |
| `isPumbleBot` | boolean |  |
| `name` | string |  |
| `phone` | string |  |
| `role` | string |  |
| `status` | string |  |
| `timeZoneId` | string |  |
| `title` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Pumble API, this operation is `GET /listUsers` (base URL `https://pumble-api-keys.addons.marketplace.cake.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

