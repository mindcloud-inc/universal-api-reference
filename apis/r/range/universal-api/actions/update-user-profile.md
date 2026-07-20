# Range: Update User Profile

Update a user's profile fields with partial profile data.

```
PUT https://connect.mindcloud.co/v1/universal/range/latest/actions/update-user-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Range `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/range/latest/actions/update-user-profile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/range/latest/actions/update-user-profile', {
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
| `profile` | object | no | Full or partial user profile object. |
| `userId` | string | no | The Range user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "altEmail": "ava@example.com",
      "birthDate": "string",
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "fullName": "Ava Chen",
      "location": "string",
      "mascot": "string",
      "measurementSystem": "string",
      "mood": "string",
      "moodColor": "string",
      "moodContext": "string",
      "myersBriggs": "string",
      "phoneCell": "string",
      "phoneWork": "string",
      "profilePhoto": "string",
      "profilePhotoSrcset": {},
      "pronounciation": "string",
      "pronouns": "string",
      "purpose": "string",
      "referralType": "string",
      "roleType": "string",
      "startDate": "string",
      "timezone": "string",
      "timezoneOffset": 1,
      "trueColors": "string",
      "useCase": "string",
      "useCaseOther": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `altEmail` | string |  |
| `birthDate` | string |  |
| `displayName` | string |  |
| `email` | string |  |
| `fullName` | string |  |
| `location` | string |  |
| `mascot` | string |  |
| `measurementSystem` | string |  |
| `mood` | string |  |
| `moodColor` | string |  |
| `moodContext` | string |  |
| `myersBriggs` | string |  |
| `phoneCell` | string |  |
| `phoneWork` | string |  |
| `profilePhoto` | string |  |
| `profilePhotoSrcset` | object |  |
| `pronounciation` | string |  |
| `pronouns` | string |  |
| `purpose` | string |  |
| `referralType` | string |  |
| `roleType` | string |  |
| `startDate` | string |  |
| `timezone` | string |  |
| `timezoneOffset` | number |  |
| `trueColors` | string |  |
| `useCase` | string |  |
| `useCaseOther` | string |  |

## Native endpoint

Through the native Range API, this operation is `PUT /v1/users/:userId/profile` (base URL `https://api.range.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user-profile.md) for the provider-specific parameters and requirements.

