# ProjectManager: Retrieve Resource

Retrieves a resource from ProjectManager.

```
GET https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/retrieve-resource
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProjectManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/retrieve-resource?connectionId=$CONNECTION_ID&resourceId=33333333-3333-3333-3333-333333333333" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resourceId": "33333333-3333-3333-3333-333333333333"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/retrieve-resource?${params}`, {
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
| `resourceId` | string | yes | The id of the Resource Example: `33333333-3333-3333-3333-333333333333`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approver": {
        "id": "string",
        "name": "Ava Chen"
      },
      "avatarUrl": "https://example.com",
      "city": "string",
      "color": "string",
      "colorName": "Ava Chen",
      "country": "string",
      "countryName": "Ava Chen",
      "createdBy": "string",
      "createdDate": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "hourlyRate": 1,
      "id": "string",
      "initials": "string",
      "isActive": true,
      "language": "string",
      "lastName": "Chen",
      "modifiedBy": "string",
      "modifiedDate": "string",
      "name": "Ava Chen",
      "notes": "string",
      "onlineDateTime": "string",
      "phone": "string",
      "resourceTypeId": 1,
      "role": "string",
      "skills": {
        "id": "string",
        "inUse": true,
        "name": "Ava Chen"
      },
      "state": "string",
      "teams": {
        "id": "string",
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approver.id` | string |  |
| `approver.name` | string |  |
| `avatarUrl` | string |  |
| `city` | string |  |
| `color` | string |  |
| `colorName` | string |  |
| `country` | string |  |
| `countryName` | string |  |
| `createdBy` | string |  |
| `createdDate` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `hourlyRate` | number |  |
| `id` | string |  |
| `initials` | string |  |
| `isActive` | boolean |  |
| `language` | string |  |
| `lastName` | string |  |
| `modifiedBy` | string |  |
| `modifiedDate` | string |  |
| `name` | string |  |
| `notes` | string |  |
| `onlineDateTime` | string |  |
| `phone` | string |  |
| `resourceTypeId` | number |  |
| `role` | string |  |
| `skills.id` | string |  |
| `skills.inUse` | boolean |  |
| `skills.name` | string |  |
| `state` | string |  |
| `teams.id` | string |  |
| `teams.name` | string |  |

## Native endpoint

Through the native ProjectManager API, this operation is `GET /api/data/resources/:resourceId` (base URL `https://api.projectmanager.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-resource.md) for the provider-specific parameters and requirements.

