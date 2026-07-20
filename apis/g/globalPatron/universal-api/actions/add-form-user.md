# Global Patron: Add Form User

Adds a form user in Global Patron.

```
POST https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/add-form-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Global Patron `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/add-form-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "collaboratorEmail": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/add-form-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string",
    "collaboratorEmail": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | ID of the form. |
| `collaboratorEmail` | string | yes | Email address of the collaborator to add. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hasFormSubmission` | boolean | no | Whether the collaborator can view form submissions. |
| `editFormSubmission` | boolean | no | Whether the collaborator can edit form submissions. |
| `hasReport` | boolean | no | Whether the collaborator can view reports. |
| `editForm` | boolean | no | Whether the collaborator can edit the form. |
| `editOthersFormSubmission` | boolean | no | Whether the collaborator can edit other users' submissions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionSuccessful": true,
      "error": "string",
      "id": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionSuccessful` | boolean | Whether GlobalPatron reports the action was successful. |
| `error` | string | Provider error message when present. |
| `id` | string | Created user security record identifier. |
| `message` | string | Provider status message. |

## Native endpoint

Through the native Global Patron API, this operation is `POST /api/restricted/form/{formId}/usersecurity` (base URL `https://api.globalpatron.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-form-user.md) for the provider-specific parameters and requirements.

