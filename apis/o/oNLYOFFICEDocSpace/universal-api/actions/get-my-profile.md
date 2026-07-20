# ONLYOFFICE DocSpace: Get My Profile

Retrieves your profile from ONLYOFFICE DocSpace.

```
GET https://connect.mindcloud.co/v1/universal/oNLYOFFICEDocSpace/latest/actions/get-my-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ONLYOFFICE DocSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oNLYOFFICEDocSpace/latest/actions/get-my-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oNLYOFFICEDocSpace/latest/actions/get-my-profile?${params}`, {
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
      "activationStatus": 1,
      "avatar": "string",
      "avatarMax": "string",
      "avatarMedium": "string",
      "avatarOriginal": "string",
      "avatarSmall": "string",
      "department": "string",
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "firstName": "Ava",
      "hasAvatar": true,
      "hasPersonalFolder": true,
      "id": "string",
      "isAdmin": true,
      "isAnonim": true,
      "isCollaborator": true,
      "isLDAP": true,
      "isOwner": true,
      "isRoomAdmin": true,
      "isSSO": true,
      "isVisitor": true,
      "lastName": "Chen",
      "loginEventId": 1,
      "mobilePhoneActivationStatus": 1,
      "profileUrl": "https://example.com",
      "registrationDate": "2026-05-07T12:00:00.000Z",
      "status": 1,
      "theme": "string",
      "userName": "Ava Chen",
      "workFrom": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activationStatus` | number |  |
| `avatar` | string |  |
| `avatarMax` | string |  |
| `avatarMedium` | string |  |
| `avatarOriginal` | string |  |
| `avatarSmall` | string |  |
| `department` | string |  |
| `displayName` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `hasAvatar` | boolean |  |
| `hasPersonalFolder` | boolean |  |
| `id` | string |  |
| `isAdmin` | boolean |  |
| `isAnonim` | boolean |  |
| `isCollaborator` | boolean |  |
| `isLDAP` | boolean |  |
| `isOwner` | boolean |  |
| `isRoomAdmin` | boolean |  |
| `isSSO` | boolean |  |
| `isVisitor` | boolean |  |
| `lastName` | string |  |
| `loginEventId` | number |  |
| `mobilePhoneActivationStatus` | number |  |
| `profileUrl` | string |  |
| `registrationDate` | date |  |
| `status` | number |  |
| `theme` | string |  |
| `userName` | string |  |
| `workFrom` | date |  |

## Native endpoint

Through the native ONLYOFFICE DocSpace API, this operation is `GET /api/2.0/people/@self` (base URL `https://docspace-t0dtrp.onlyoffice.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-my-profile.md) for the provider-specific parameters and requirements.

