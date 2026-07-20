# CoordinateHQ Universal API Examples

These examples use the MindCloud API key and CoordinateHQ connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Download Task File



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coordinateHQ/latest/actions/download-task-file?connectionId=$CONNECTION_ID&project_id=string&task_id=string&file_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project_id": "string",
  "task_id": "string",
  "file_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coordinateHQ/latest/actions/download-task-file?${params}`, {
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
      "customers": [
        {
          "customerId": "string",
          "customerName": "Ava Chen"
        }
      ],
      "entityType": "string",
      "entityUrl": "https://example.com",
      "externalObjectId": {},
      "groupId": "string",
      "lastModifiedDt": "string",
      "projectExternalObjectId": {},
      "projectId": "string",
      "projectName": "Ava Chen",
      "taskAssigneeStakeholderEmailAddress": {},
      "taskAssigneeStakeholderFullName": {},
      "taskAssigneeStakeholderId": {},
      "taskCompletedByEmail": {},
      "taskCompletedByName": {},
      "taskCompletedDt": {},
      "taskDescription": {},
      "taskDueDate": "string",
      "taskGroupTitle": "string",
      "taskId": "string",
      "taskInternal": {},
      "taskStartDate": {},
      "taskStatusCurrent": {},
      "taskStatusCurrentDt": {},
      "taskTitle": "string",
      "vendorId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Download Task File action reference](actions/download-task-file.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/coordinateHQ/latest/actions/download-task-file).

## Add Organization Stakeholder



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coordinateHQ/latest/actions/add-organization-stakeholder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coordinateHQ/latest/actions/add-organization-stakeholder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "string"
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
      "entityType": "string",
      "externalObjectId": {},
      "lastModifiedDt": "string",
      "stakeholderEmailAddress": "ava@example.com",
      "stakeholderFullName": {},
      "stakeholderId": "string",
      "stakeholderPhone": {},
      "stakeholderProjectId": "string",
      "stakeholderRelatedOrgId": "string",
      "stakeholderTitle": {},
      "vendorId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Organization Stakeholder action reference](actions/add-organization-stakeholder.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/coordinateHQ/latest/actions/add-organization-stakeholder).
