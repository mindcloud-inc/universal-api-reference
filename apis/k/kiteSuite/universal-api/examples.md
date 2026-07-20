# KiteSuite Universal API Examples

These examples use the MindCloud API key and KiteSuite connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Workspace Roles

Retrieves workspace roles from KiteSuite.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/list-workspace-roles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/list-workspace-roles?${params}`, {
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
      "completeSprint": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "createCustomFields": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "createCustomRole": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "createdAt": "string",
      "createDoc": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "createEpic": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "createList": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "createProject": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "createProjectCustomRole": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "createProjectDoc": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "createSprint": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "createTask": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "deleteCustomFields": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "deleteCustomRole": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "deleteDoc": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "deleteEpic": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "deleteList": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "deleteProject": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "deleteProjectCustomRole": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "deleteProjectDoc": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "deleteSprint": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "deleteTask": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "exportCsv": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "Id": "string",
      "importCsv": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "inviteUserProject": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "inviteUserWorkSpace": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "isDefault": true,
      "manageFields": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "manageIdentity": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "removeUserProject": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "removeUserWorkSpace": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "roleName": "Ava Chen",
      "sendMessage": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "sendMessageProject": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "startSprint": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "updateAdminRole": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "updateCustomFields": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "updateCustomRole": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "updatedAt": "string",
      "updateDoc": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "updateEpic": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "updateList": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "updateOganisationAvatar": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "updateProject": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "updateProjectAdminRole": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "updateProjectCustomRole": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "updateProjectDoc": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "updateSprint": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "updateSubscription": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "updateTask": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "updateUserRoleProject": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "updateUserRoleWorkSpace": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "V": 1,
      "viewDoc": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "viewEpic": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "viewProjectDoc": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "viewReports": {
        "description": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "viewSprint": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "viewTask": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "viewTimesheet": {
        "description": "string",
        "groupID": "string",
        "isProjectPermission": true,
        "lable": "string",
        "value": true
      },
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Workspace Roles action reference](actions/list-workspace-roles.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kiteSuite/latest/actions/list-workspace-roles).

## Add Project Member

Adds a member to a project in KiteSuite.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/add-project-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectID": "string",
  "members[]": [
    "string"
  ],
  "roleID": "e.g. 69d3e6b9353b6b2d2a539a11"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/add-project-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectID": "string",
    "members[]": ["string"],
    "roleID": "e.g. 69d3e6b9353b6b2d2a539a11"
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
      "_id": "string",
      "active": true,
      "member": {},
      "role": {}
    }
  ],
  "meta": {}
}
```

See the full [Add Project Member action reference](actions/add-project-member.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kiteSuite/latest/actions/add-project-member).
