# ProjectManager: Update Resource

Updates an existing resource in ProjectManager.

```
PUT https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/update-resource
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProjectManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/update-resource" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "resourceId": "33333333-3333-3333-3333-333333333333"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/update-resource', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "resourceId": "33333333-3333-3333-3333-333333333333"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `resourceId` | string | yes | The id of the resource Example: `33333333-3333-3333-3333-333333333333`. |
| `firstName` | string | no | The first name of the person Resource. Applies to personnel Resources only. Example: `Update Resource First Name`. |
| `lastName` | string | no | The last name of the person Resource. Applies to personnel Resources only. Example: `Update Resource Last Name`. |
| `email` | string | no | The email address of this Resource. Note that this email cannot be changed once it has been assigned. Example: `apps@mindcloud.co`. |
| `hourlyRate` | number | no | The basic hourly rate for this Resource. Example: `1`. |
| `phone` | string | no | The phone number associated with this Resource. Example: `+15555550123`. |
| `city` | string | no | The city where this Resource is located. Example: `sample-city`. |
| `state` | string | no | The state or region where this Resource is located. This value is not constrained to a list of known states or regions. Example: `sample-state`. |
| `countryCode` | string | no | A text field indicating the country in which this Resource is located. This value must be one of the following: US, NZ, AU. Example: `sample-countrycode`. |
| `notes` | string | no | Free-form text notes about this Resource. You may use this field to store extra information about the Resource. Example: `MindCloud sample notes.`. |
| `roleId` | string | no | The Role Id associated with this Resource. Applies to personnel Resources only. Example: `88888888-8888-8888-8888-888888888888`. |
| `teamIds[]` | array<string> | no | The list of ResourceTeams to which this Resource belongs. Example: `sample`. |
| `teamIds[]` | array<string> | no | The list of ResourceTeams to which this Resource belongs. Example: `sample`. |
| `teamIds[]` | array<string> | no | The list of ResourceTeams to which this Resource belongs. Example: `sample`. |
| `skillIds[]` | array<string> | no | The list of ResourceSkills possessed by this Resource. Example: `sample`. |
| `skillIds[]` | array<string> | no | The list of ResourceSkills possessed by this Resource. Example: `sample`. |
| `skillIds[]` | array<string> | no | The list of ResourceSkills possessed by this Resource. Example: `sample`. |
| `isActive` | boolean | no | Active/Inactive the Resource. Example: `true`. |
| `approverId` | string | no | The Approver Id associated with this Resource. Applies to personnel Resources only. Example: `88888888-8888-8888-8888-888888888888`. |
| `colorName` | string | no | Collaboration Color for this resource. eg. teal, cyan, lightblue, blurple, purple, pink, orange, gray Example: `#336699`. |
| `language` | string | no | Translation Language for this resource. e.g. en-US, en-GB, fr-FR, es-ES Example: `sample-language`. |

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

Through the native ProjectManager API, this operation is `PUT /api/data/resources/:resourceId` (base URL `https://api.projectmanager.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-resource.md) for the provider-specific parameters and requirements.

