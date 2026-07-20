# ProjectManager: Retrieve Me

Retrieves current user details from ProjectManager.

```
GET https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/retrieve-me
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProjectManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/retrieve-me?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/retrieve-me?${params}`, {
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
      "emailAddress": "ava@example.com",
      "fullName": "Ava Chen",
      "id": "string",
      "isAccountAdministrator": true,
      "isGlobalAdmin": true,
      "links": {
        "project": "https://example.com",
        "workSpaceApi": "https://example.com"
      },
      "location": "string",
      "permissions": {
        "approveTimesheet": true,
        "createProject": true,
        "editAccount": true,
        "editAllProjects": true,
        "editAllTimesheets": true,
        "editCost": true,
        "editHoliday": true,
        "editIntegration": true,
        "editProjectField": true,
        "editRole": true,
        "editUser": true,
        "editUserField": true,
        "exportProject": true,
        "inviteUser": true,
        "setUpBoardWorkflow": true,
        "viewMyBoard": true,
        "viewUser": true
      },
      "roleName": "Ava Chen",
      "workSpaceCountry": "string",
      "workSpaceCountryCode": "string",
      "workSpaceId": "string",
      "workSpaceIsActive": true,
      "workSpaceName": "Ava Chen",
      "workSpaceStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `emailAddress` | string |  |
| `fullName` | string |  |
| `id` | string |  |
| `isAccountAdministrator` | boolean |  |
| `isGlobalAdmin` | boolean |  |
| `links.project` | string |  |
| `links.workSpaceApi` | string |  |
| `location` | string |  |
| `permissions.approveTimesheet` | boolean |  |
| `permissions.createProject` | boolean |  |
| `permissions.editAccount` | boolean |  |
| `permissions.editAllProjects` | boolean |  |
| `permissions.editAllTimesheets` | boolean |  |
| `permissions.editCost` | boolean |  |
| `permissions.editHoliday` | boolean |  |
| `permissions.editIntegration` | boolean |  |
| `permissions.editProjectField` | boolean |  |
| `permissions.editRole` | boolean |  |
| `permissions.editUser` | boolean |  |
| `permissions.editUserField` | boolean |  |
| `permissions.exportProject` | boolean |  |
| `permissions.inviteUser` | boolean |  |
| `permissions.setUpBoardWorkflow` | boolean |  |
| `permissions.viewMyBoard` | boolean |  |
| `permissions.viewUser` | boolean |  |
| `roleName` | string |  |
| `workSpaceCountry` | string |  |
| `workSpaceCountryCode` | string |  |
| `workSpaceId` | string |  |
| `workSpaceIsActive` | boolean |  |
| `workSpaceName` | string |  |
| `workSpaceStatus` | string |  |

## Native endpoint

Through the native ProjectManager API, this operation is `GET /api/data/me` (base URL `https://api.projectmanager.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-me.md) for the provider-specific parameters and requirements.

