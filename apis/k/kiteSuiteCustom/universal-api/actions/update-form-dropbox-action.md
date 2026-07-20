# Kite Suite: Update Form Dropbox Action



```
PUT https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-form-dropbox-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-form-dropbox-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "id": "string",
  "actionName": "Ava Chen",
  "subFolderName": "Ava Chen",
  "isCreateSubFolder": true,
  "sendSubmissionFormat": "string",
  "selectedFields[]": [
    "string"
  ],
  "isDisabled": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-form-dropbox-action', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "id": "string",
    "actionName": "Ava Chen",
    "subFolderName": "Ava Chen",
    "isCreateSubFolder": true,
    "sendSubmissionFormat": "string",
    "selectedFields[]": ["string"],
    "isDisabled": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | Request body |
| `id` | string | yes | ID of the Dropbox action to update. |
| `actionName` | string | yes | Updated name of the Dropbox action. |
| `subFolderName` | string | yes | Updated subfolder name. |
| `isCreateSubFolder` | boolean | yes | Updated flag to create a subfolder. |
| `sendSubmissionFormat` | string | yes | Updated submission format. |
| `selectedFields[]` | array | yes | Updated array of form element IDs to include in the upload. |
| `isDisabled` | boolean | yes | Flag to disable the action. |

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
| `value` | object | Updated form integration object. |

## Native endpoint

Through the native Kite Suite API, this operation is `PATCH /api/v1/form/integration/dropbox/actions/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-form-dropbox-action.md) for the provider-specific parameters and requirements.

