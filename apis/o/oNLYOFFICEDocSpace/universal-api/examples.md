# ONLYOFFICE DocSpace Universal API Examples

These examples use the MindCloud API key and ONLYOFFICE DocSpace connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get My Profile

Retrieves your profile from ONLYOFFICE DocSpace.

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

Example response:

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

See the full [Get My Profile action reference](actions/get-my-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/oNLYOFFICEDocSpace/latest/actions/get-my-profile).
