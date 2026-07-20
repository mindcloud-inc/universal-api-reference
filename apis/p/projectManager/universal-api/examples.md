# ProjectManager Universal API Examples

These examples use the MindCloud API key and ProjectManager connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Retrieve Me

Retrieves current user details from ProjectManager.

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

Example response:

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

See the full [Retrieve Me action reference](actions/retrieve-me.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/projectManager/latest/actions/retrieve-me).

## Add TaskTag to Task

Adds a task tag to a task in ProjectManager.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/add-task-tag-to-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "22222222-2222-2222-2222-222222222222",
  "value[]": "sample"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/add-task-tag-to-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "22222222-2222-2222-2222-222222222222",
    "value[]": "sample",
    "value[]": "sample",
    "value[]": "sample",
    "value[]": "sample"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "changeSetId": "string",
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add TaskTag to Task action reference](actions/add-task-tag-to-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/projectManager/latest/actions/add-task-tag-to-task).
