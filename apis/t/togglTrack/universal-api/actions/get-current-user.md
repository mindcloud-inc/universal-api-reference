# Toggl Track: Get Current User

Retrieves the current user from Toggl Track.

```
GET https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toggl Track `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/get-current-user?${params}`, {
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
| `withRelatedData` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiToken": "string",
      "at": "string",
      "authorizationUpdatedAt": "string",
      "beginningOfWeek": 1,
      "countryId": 1,
      "createdAt": "string",
      "defaultWorkspaceId": 1,
      "email": "ava@example.com",
      "fullname": "Ava Chen",
      "hasPassword": true,
      "id": 1,
      "imageUrl": "https://example.com",
      "oauthProviders": [
        "string"
      ],
      "openidEmail": {},
      "openidEnabled": true,
      "timezone": "string",
      "togglAccountsId": "string",
      "twoFaEnabled": true,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiToken` | string |  |
| `at` | string |  |
| `authorizationUpdatedAt` | string |  |
| `beginningOfWeek` | number |  |
| `countryId` | number |  |
| `createdAt` | string |  |
| `defaultWorkspaceId` | number |  |
| `email` | string |  |
| `fullname` | string |  |
| `hasPassword` | boolean |  |
| `id` | number |  |
| `imageUrl` | string |  |
| `oauthProviders[]` | string |  |
| `openidEmail` | object |  |
| `openidEnabled` | boolean |  |
| `timezone` | string |  |
| `togglAccountsId` | string |  |
| `twoFaEnabled` | boolean |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Toggl Track API, this operation is `GET /api/v9/me` (base URL `https://api.track.toggl.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

