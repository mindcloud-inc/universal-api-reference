# Follow Up Boss: Get User

Retrieves a user from Follow Up Boss.

```
GET https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Follow Up Boss `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/get-user?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/get-user?${params}`, {
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
| `id` | string | yes | The user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acceptedShowingtimeConsent": true,
      "acceptedShowingtimeConsentV2": true,
      "beta": true,
      "canCreateApiKeys": true,
      "canExport": true,
      "created": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "fuid": "string",
      "groups": [
        {}
      ],
      "id": 1,
      "isOwner": true,
      "lastName": "Chen",
      "lastSeenAndroid": "2026-05-07T12:00:00.000Z",
      "lastSeenFub2": "2026-05-07T12:00:00.000Z",
      "lastSeenIos": "2026-05-07T12:00:00.000Z",
      "leadEmailAddress": "ava@example.com",
      "name": "Ava Chen",
      "pauseLeadDistribution": true,
      "phone": "string",
      "picture": {},
      "role": "string",
      "status": "string",
      "teamIds": [
        1
      ],
      "teamLeaderOf": [
        1
      ],
      "timezone": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acceptedShowingtimeConsent` | boolean |  |
| `acceptedShowingtimeConsentV2` | boolean |  |
| `beta` | boolean |  |
| `canCreateApiKeys` | boolean |  |
| `canExport` | boolean |  |
| `created` | date |  |
| `email` | string |  |
| `firstName` | string |  |
| `fuid` | string |  |
| `groups` | array<object> |  |
| `id` | number |  |
| `isOwner` | boolean |  |
| `lastName` | string |  |
| `lastSeenAndroid` | date |  |
| `lastSeenFub2` | date |  |
| `lastSeenIos` | date |  |
| `leadEmailAddress` | string |  |
| `name` | string |  |
| `pauseLeadDistribution` | boolean |  |
| `phone` | string |  |
| `picture` | object |  |
| `role` | string |  |
| `status` | string |  |
| `teamIds` | array<number> |  |
| `teamLeaderOf` | array<number> |  |
| `timezone` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native Follow Up Boss API, this operation is `GET users/:id` (base URL `https://api.followupboss.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

