# Zoho Projects: Get User Details

Retrieves user details from Zoho Projects.

```
GET https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/get-user-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Projects `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/get-user-details?connectionId=$CONNECTION_ID&portalId=string&userRef=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "portalId": "string",
  "userRef": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/get-user-details?${params}`, {
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
| `portalId` | string | yes | Zoho Projects portal ID. |
| `userRef` | string | yes | Zoho Projects user ZPUID or email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addedTime": "2026-05-07T12:00:00.000Z",
      "associatedServices": [
        [
          "string"
        ]
      ],
      "budget": "string",
      "businessHours": {
        "id": "string",
        "name": "Ava Chen",
        "version": 1,
        "workingHours": [
          [
            {}
          ]
        ]
      },
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "id": "string",
      "isActive": true,
      "isConfirmed": true,
      "lastAccessedOn": "2026-05-07T12:00:00.000Z",
      "lastName": "Chen",
      "profile": {
        "id": "string",
        "isDefault": true,
        "name": "Ava Chen",
        "type": "string"
      },
      "role": {
        "id": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "status": "string",
      "timeOfRequest": "string",
      "updatedTime": "2026-05-07T12:00:00.000Z",
      "userType": "string",
      "zuid": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addedTime` | date |  |
| `associatedServices[]` | array<string> |  |
| `budget` | string |  |
| `businessHours.id` | string |  |
| `businessHours.name` | string |  |
| `businessHours.version` | number |  |
| `businessHours.workingHours[]` | array<object> |  |
| `displayName` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `fullName` | string |  |
| `id` | string |  |
| `isActive` | boolean |  |
| `isConfirmed` | boolean |  |
| `lastAccessedOn` | date |  |
| `lastName` | string |  |
| `profile.id` | string |  |
| `profile.isDefault` | boolean |  |
| `profile.name` | string |  |
| `profile.type` | string |  |
| `role.id` | string |  |
| `role.name` | string |  |
| `role.type` | string |  |
| `status` | string |  |
| `timeOfRequest` | string |  |
| `updatedTime` | date |  |
| `userType` | string |  |
| `zuid` | number |  |

## Native endpoint

Through the native Zoho Projects API, this operation is `GET /portal/[:PORTALID]/users/[:USERREF]` (base URL `https://projectsapi.zoho.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-details.md) for the provider-specific parameters and requirements.

