# Smartcat Universal API Examples

These examples use the MindCloud API key and Smartcat connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account

Retrieves account details from the current Smartcat account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/get-account?${params}`, {
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
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "endCustomerValue": "string",
      "id": "string",
      "interInstallationAccountId": "string",
      "isDisabled": true,
      "isPersonal": true,
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Account action reference](actions/get-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/smartcat/latest/actions/get-account).

## Add Project Document

Adds a document to a Smartcat project.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/add-project-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "project-id",
  "request": "[object Object],[object Object]",
  "FILE_1": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/add-project-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "project-id",
    "request": "[object Object],[object Object]",
    "FILE_1": "string"
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
      "creationDate": "2026-05-07T12:00:00.000Z",
      "deadline": "2026-05-07T12:00:00.000Z",
      "documentDisassemblingStatus": "string",
      "externalId": "string",
      "filename": "Ava Chen",
      "fullPath": "string",
      "id": "string",
      "name": "Ava Chen",
      "placeholdersAreEnabled": true,
      "pretranslateCompleted": true,
      "projectId": "string",
      "readyForCompletion": true,
      "revisionLabel": "string",
      "sourceLanguage": "string",
      "status": "string",
      "targetLanguage": "string",
      "wordsCount": 1,
      "workflowStages": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Add Project Document action reference](actions/add-project-document.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/smartcat/latest/actions/add-project-document).
