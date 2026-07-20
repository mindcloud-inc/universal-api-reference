# KiteSuite: List Workspace Roles

Retrieves workspace roles from KiteSuite.

```
GET https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/list-workspace-roles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KiteSuite `connectionId` ([setup](../authentication.md)).

## Example request

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



## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completeSprint.description` | string |  |
| `completeSprint.groupID` | string |  |
| `completeSprint.isProjectPermission` | boolean |  |
| `completeSprint.lable` | string |  |
| `completeSprint.value` | boolean |  |
| `createCustomFields.description` | string |  |
| `createCustomFields.groupID` | string |  |
| `createCustomFields.isProjectPermission` | boolean |  |
| `createCustomFields.lable` | string |  |
| `createCustomFields.value` | boolean |  |
| `createCustomRole.description` | string |  |
| `createCustomRole.groupID` | string |  |
| `createCustomRole.isProjectPermission` | boolean |  |
| `createCustomRole.lable` | string |  |
| `createCustomRole.value` | boolean |  |
| `createdAt` | string |  |
| `createDoc.description` | string |  |
| `createDoc.groupID` | string |  |
| `createDoc.isProjectPermission` | boolean |  |
| `createDoc.lable` | string |  |
| `createDoc.value` | boolean |  |
| `createEpic.description` | string |  |
| `createEpic.groupID` | string |  |
| `createEpic.isProjectPermission` | boolean |  |
| `createEpic.lable` | string |  |
| `createEpic.value` | boolean |  |
| `createList.description` | string |  |
| `createList.groupID` | string |  |
| `createList.isProjectPermission` | boolean |  |
| `createList.lable` | string |  |
| `createList.value` | boolean |  |
| `createProject.description` | string |  |
| `createProject.groupID` | string |  |
| `createProject.isProjectPermission` | boolean |  |
| `createProject.lable` | string |  |
| `createProject.value` | boolean |  |
| `createProjectCustomRole.description` | string |  |
| `createProjectCustomRole.groupID` | string |  |
| `createProjectCustomRole.isProjectPermission` | boolean |  |
| `createProjectCustomRole.lable` | string |  |
| `createProjectCustomRole.value` | boolean |  |
| `createProjectDoc.description` | string |  |
| `createProjectDoc.groupID` | string |  |
| `createProjectDoc.isProjectPermission` | boolean |  |
| `createProjectDoc.lable` | string |  |
| `createProjectDoc.value` | boolean |  |
| `createSprint.description` | string |  |
| `createSprint.groupID` | string |  |
| `createSprint.isProjectPermission` | boolean |  |
| `createSprint.lable` | string |  |
| `createSprint.value` | boolean |  |
| `createTask.description` | string |  |
| `createTask.groupID` | string |  |
| `createTask.isProjectPermission` | boolean |  |
| `createTask.lable` | string |  |
| `createTask.value` | boolean |  |
| `deleteCustomFields.description` | string |  |
| `deleteCustomFields.groupID` | string |  |
| `deleteCustomFields.isProjectPermission` | boolean |  |
| `deleteCustomFields.lable` | string |  |
| `deleteCustomFields.value` | boolean |  |
| `deleteCustomRole.description` | string |  |
| `deleteCustomRole.groupID` | string |  |
| `deleteCustomRole.isProjectPermission` | boolean |  |
| `deleteCustomRole.lable` | string |  |
| `deleteCustomRole.value` | boolean |  |
| `deleteDoc.description` | string |  |
| `deleteDoc.groupID` | string |  |
| `deleteDoc.isProjectPermission` | boolean |  |
| `deleteDoc.lable` | string |  |
| `deleteDoc.value` | boolean |  |
| `deleteEpic.description` | string |  |
| `deleteEpic.groupID` | string |  |
| `deleteEpic.isProjectPermission` | boolean |  |
| `deleteEpic.lable` | string |  |
| `deleteEpic.value` | boolean |  |
| `deleteList.description` | string |  |
| `deleteList.groupID` | string |  |
| `deleteList.isProjectPermission` | boolean |  |
| `deleteList.lable` | string |  |
| `deleteList.value` | boolean |  |
| `deleteProject.description` | string |  |
| `deleteProject.groupID` | string |  |
| `deleteProject.isProjectPermission` | boolean |  |
| `deleteProject.lable` | string |  |
| `deleteProject.value` | boolean |  |
| `deleteProjectCustomRole.description` | string |  |
| `deleteProjectCustomRole.groupID` | string |  |
| `deleteProjectCustomRole.isProjectPermission` | boolean |  |
| `deleteProjectCustomRole.lable` | string |  |
| `deleteProjectCustomRole.value` | boolean |  |
| `deleteProjectDoc.description` | string |  |
| `deleteProjectDoc.groupID` | string |  |
| `deleteProjectDoc.isProjectPermission` | boolean |  |
| `deleteProjectDoc.lable` | string |  |
| `deleteProjectDoc.value` | boolean |  |
| `deleteSprint.description` | string |  |
| `deleteSprint.groupID` | string |  |
| `deleteSprint.isProjectPermission` | boolean |  |
| `deleteSprint.lable` | string |  |
| `deleteSprint.value` | boolean |  |
| `deleteTask.description` | string |  |
| `deleteTask.groupID` | string |  |
| `deleteTask.isProjectPermission` | boolean |  |
| `deleteTask.lable` | string |  |
| `deleteTask.value` | boolean |  |
| `exportCsv.description` | string |  |
| `exportCsv.groupID` | string |  |
| `exportCsv.isProjectPermission` | boolean |  |
| `exportCsv.lable` | string |  |
| `exportCsv.value` | boolean |  |
| `Id` | string |  |
| `importCsv.description` | string |  |
| `importCsv.groupID` | string |  |
| `importCsv.isProjectPermission` | boolean |  |
| `importCsv.lable` | string |  |
| `importCsv.value` | boolean |  |
| `inviteUserProject.description` | string |  |
| `inviteUserProject.groupID` | string |  |
| `inviteUserProject.isProjectPermission` | boolean |  |
| `inviteUserProject.lable` | string |  |
| `inviteUserProject.value` | boolean |  |
| `inviteUserWorkSpace.description` | string |  |
| `inviteUserWorkSpace.groupID` | string |  |
| `inviteUserWorkSpace.isProjectPermission` | boolean |  |
| `inviteUserWorkSpace.lable` | string |  |
| `inviteUserWorkSpace.value` | boolean |  |
| `isDefault` | boolean |  |
| `manageFields.description` | string |  |
| `manageFields.groupID` | string |  |
| `manageFields.isProjectPermission` | boolean |  |
| `manageFields.lable` | string |  |
| `manageFields.value` | boolean |  |
| `manageIdentity.description` | string |  |
| `manageIdentity.groupID` | string |  |
| `manageIdentity.isProjectPermission` | boolean |  |
| `manageIdentity.lable` | string |  |
| `manageIdentity.value` | boolean |  |
| `removeUserProject.description` | string |  |
| `removeUserProject.groupID` | string |  |
| `removeUserProject.isProjectPermission` | boolean |  |
| `removeUserProject.lable` | string |  |
| `removeUserProject.value` | boolean |  |
| `removeUserWorkSpace.description` | string |  |
| `removeUserWorkSpace.groupID` | string |  |
| `removeUserWorkSpace.isProjectPermission` | boolean |  |
| `removeUserWorkSpace.lable` | string |  |
| `removeUserWorkSpace.value` | boolean |  |
| `roleName` | string |  |
| `sendMessage.description` | string |  |
| `sendMessage.groupID` | string |  |
| `sendMessage.isProjectPermission` | boolean |  |
| `sendMessage.lable` | string |  |
| `sendMessage.value` | boolean |  |
| `sendMessageProject.description` | string |  |
| `sendMessageProject.groupID` | string |  |
| `sendMessageProject.isProjectPermission` | boolean |  |
| `sendMessageProject.lable` | string |  |
| `sendMessageProject.value` | boolean |  |
| `startSprint.description` | string |  |
| `startSprint.groupID` | string |  |
| `startSprint.isProjectPermission` | boolean |  |
| `startSprint.lable` | string |  |
| `startSprint.value` | boolean |  |
| `updateAdminRole.description` | string |  |
| `updateAdminRole.groupID` | string |  |
| `updateAdminRole.isProjectPermission` | boolean |  |
| `updateAdminRole.lable` | string |  |
| `updateAdminRole.value` | boolean |  |
| `updateCustomFields.description` | string |  |
| `updateCustomFields.groupID` | string |  |
| `updateCustomFields.isProjectPermission` | boolean |  |
| `updateCustomFields.lable` | string |  |
| `updateCustomFields.value` | boolean |  |
| `updateCustomRole.description` | string |  |
| `updateCustomRole.groupID` | string |  |
| `updateCustomRole.isProjectPermission` | boolean |  |
| `updateCustomRole.lable` | string |  |
| `updateCustomRole.value` | boolean |  |
| `updatedAt` | string |  |
| `updateDoc.description` | string |  |
| `updateDoc.groupID` | string |  |
| `updateDoc.isProjectPermission` | boolean |  |
| `updateDoc.lable` | string |  |
| `updateDoc.value` | boolean |  |
| `updateEpic.description` | string |  |
| `updateEpic.groupID` | string |  |
| `updateEpic.isProjectPermission` | boolean |  |
| `updateEpic.lable` | string |  |
| `updateEpic.value` | boolean |  |
| `updateList.description` | string |  |
| `updateList.groupID` | string |  |
| `updateList.isProjectPermission` | boolean |  |
| `updateList.lable` | string |  |
| `updateList.value` | boolean |  |
| `updateOganisationAvatar.description` | string |  |
| `updateOganisationAvatar.groupID` | string |  |
| `updateOganisationAvatar.isProjectPermission` | boolean |  |
| `updateOganisationAvatar.lable` | string |  |
| `updateOganisationAvatar.value` | boolean |  |
| `updateProject.description` | string |  |
| `updateProject.groupID` | string |  |
| `updateProject.isProjectPermission` | boolean |  |
| `updateProject.lable` | string |  |
| `updateProject.value` | boolean |  |
| `updateProjectAdminRole.description` | string |  |
| `updateProjectAdminRole.groupID` | string |  |
| `updateProjectAdminRole.isProjectPermission` | boolean |  |
| `updateProjectAdminRole.lable` | string |  |
| `updateProjectAdminRole.value` | boolean |  |
| `updateProjectCustomRole.description` | string |  |
| `updateProjectCustomRole.groupID` | string |  |
| `updateProjectCustomRole.isProjectPermission` | boolean |  |
| `updateProjectCustomRole.lable` | string |  |
| `updateProjectCustomRole.value` | boolean |  |
| `updateProjectDoc.description` | string |  |
| `updateProjectDoc.groupID` | string |  |
| `updateProjectDoc.isProjectPermission` | boolean |  |
| `updateProjectDoc.lable` | string |  |
| `updateProjectDoc.value` | boolean |  |
| `updateSprint.description` | string |  |
| `updateSprint.groupID` | string |  |
| `updateSprint.isProjectPermission` | boolean |  |
| `updateSprint.lable` | string |  |
| `updateSprint.value` | boolean |  |
| `updateSubscription.description` | string |  |
| `updateSubscription.groupID` | string |  |
| `updateSubscription.isProjectPermission` | boolean |  |
| `updateSubscription.lable` | string |  |
| `updateSubscription.value` | boolean |  |
| `updateTask.description` | string |  |
| `updateTask.groupID` | string |  |
| `updateTask.isProjectPermission` | boolean |  |
| `updateTask.lable` | string |  |
| `updateTask.value` | boolean |  |
| `updateUserRoleProject.description` | string |  |
| `updateUserRoleProject.groupID` | string |  |
| `updateUserRoleProject.isProjectPermission` | boolean |  |
| `updateUserRoleProject.lable` | string |  |
| `updateUserRoleProject.value` | boolean |  |
| `updateUserRoleWorkSpace.description` | string |  |
| `updateUserRoleWorkSpace.groupID` | string |  |
| `updateUserRoleWorkSpace.isProjectPermission` | boolean |  |
| `updateUserRoleWorkSpace.lable` | string |  |
| `updateUserRoleWorkSpace.value` | boolean |  |
| `V` | number |  |
| `viewDoc.description` | string |  |
| `viewDoc.groupID` | string |  |
| `viewDoc.isProjectPermission` | boolean |  |
| `viewDoc.lable` | string |  |
| `viewDoc.value` | boolean |  |
| `viewEpic.description` | string |  |
| `viewEpic.groupID` | string |  |
| `viewEpic.isProjectPermission` | boolean |  |
| `viewEpic.lable` | string |  |
| `viewEpic.value` | boolean |  |
| `viewProjectDoc.description` | string |  |
| `viewProjectDoc.groupID` | string |  |
| `viewProjectDoc.isProjectPermission` | boolean |  |
| `viewProjectDoc.lable` | string |  |
| `viewProjectDoc.value` | boolean |  |
| `viewReports.description` | string |  |
| `viewReports.isProjectPermission` | boolean |  |
| `viewReports.lable` | string |  |
| `viewReports.value` | boolean |  |
| `viewSprint.description` | string |  |
| `viewSprint.groupID` | string |  |
| `viewSprint.isProjectPermission` | boolean |  |
| `viewSprint.lable` | string |  |
| `viewSprint.value` | boolean |  |
| `viewTask.description` | string |  |
| `viewTask.groupID` | string |  |
| `viewTask.isProjectPermission` | boolean |  |
| `viewTask.lable` | string |  |
| `viewTask.value` | boolean |  |
| `viewTimesheet.description` | string |  |
| `viewTimesheet.groupID` | string |  |
| `viewTimesheet.isProjectPermission` | boolean |  |
| `viewTimesheet.lable` | string |  |
| `viewTimesheet.value` | boolean |  |
| `workspace` | string |  |

## Native endpoint

Through the native KiteSuite API, this operation is `GET /api/v1/workspace-role` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspace-roles.md) for the provider-specific parameters and requirements.

