# InstantCard: Get My Profile

Retrieves the authenticated user profile from InstantCard.

```
GET https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/get-my-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InstantCard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/get-my-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/get-my-profile?${params}`, {
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
      "email": "ava@example.com",
      "id": 1,
      "organization": {
        "organizationId": 1,
        "organizationName": "Ava Chen"
      },
      "organizationId": 1,
      "organizationName": "Ava Chen",
      "settings": {
        "fullName": "Ava Chen",
        "notifications": {
          "orderConfirmation": true,
          "orderPrintedConfirmation": true
        },
        "pageSize": 1,
        "showPhoto": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `id` | number |  |
| `organization.organizationId` | number |  |
| `organization.organizationName` | string |  |
| `organizationId` | number |  |
| `organizationName` | string |  |
| `settings.fullName` | string |  |
| `settings.notifications.orderConfirmation` | boolean |  |
| `settings.notifications.orderPrintedConfirmation` | boolean |  |
| `settings.pageSize` | number |  |
| `settings.showPhoto` | boolean |  |

## Native endpoint

Through the native InstantCard API, this operation is `GET /api/v2/profile/me` (base URL `https://core.instantcard.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-my-profile.md) for the provider-specific parameters and requirements.

