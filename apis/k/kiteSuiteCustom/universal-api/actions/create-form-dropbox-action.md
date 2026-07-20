# Kite Suite: Create Form Dropbox Action



```
POST https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/create-form-dropbox-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/create-form-dropbox-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "form": "string",
  "actionName": "Ava Chen",
  "subFolderName": "Ava Chen",
  "isCreateSubFolder": true,
  "folderName": "Ava Chen",
  "sendSubmissionFormat": "string",
  "selectedFields[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/create-form-dropbox-action', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "form": "string",
    "actionName": "Ava Chen",
    "subFolderName": "Ava Chen",
    "isCreateSubFolder": true,
    "folderName": "Ava Chen",
    "sendSubmissionFormat": "string",
    "selectedFields[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | Request body |
| `form` | string | yes | ID of the form. |
| `actionName` | string | yes | Name of the Dropbox action. |
| `subFolderName` | string | yes | Subfolder name. |
| `isCreateSubFolder` | boolean | yes | Flag to create a subfolder. |
| `folderName` | string | yes | Name of the Dropbox folder. |
| `sendSubmissionFormat` | string | yes | Submission format. |
| `selectedFields[]` | array | yes | Array of form element IDs to include in the upload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | object | Created form integration object. |

## Native endpoint

Through the native Kite Suite API, this operation is `POST /api/v1/form/integration/dropbox/actions` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-form-dropbox-action.md) for the provider-specific parameters and requirements.

