# Mendeley: Update My Profile



```
PUT https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/update-my-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendeley `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/update-my-profile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/update-my-profile', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `academicStatus` | string | no | Academic status value for the profile. |
| `biography` | string | no | Short profile biography. |
| `title` | string | no | Profile title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "academicStatus": "string",
      "created": "string",
      "discipline": {},
      "disciplines": [
        {}
      ],
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "firstName": "Ava",
      "folder": "string",
      "id": "string",
      "lastName": "Chen",
      "link": "https://example.com",
      "memberType": "string",
      "photo": {},
      "photos": [
        {}
      ],
      "privacyRestrictedView": true,
      "userType": "string",
      "verified": true,
      "visibility": "string",
      "webUserId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `academicStatus` | string |  |
| `created` | string |  |
| `discipline` | object |  |
| `disciplines` | array<object> |  |
| `displayName` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `folder` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `link` | string |  |
| `memberType` | string |  |
| `photo` | object |  |
| `photos` | array<object> |  |
| `privacyRestrictedView` | boolean |  |
| `userType` | string |  |
| `verified` | boolean |  |
| `visibility` | string |  |
| `webUserId` | number |  |

## Native endpoint

Through the native Mendeley API, this operation is `PATCH /profiles/me` (base URL `https://api.mendeley.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-my-profile.md) for the provider-specific parameters and requirements.

