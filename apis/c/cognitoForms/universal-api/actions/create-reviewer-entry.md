# Cognito Forms: Create Reviewer Entry



```
POST https://connect.mindcloud.co/v1/universal/cognitoForms/latest/actions/create-reviewer-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cognito Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cognitoForms/latest/actions/create-reviewer-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cognitoForms/latest/actions/create-reviewer-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | The ID of the Form for which you want to create an Entry |
| `Entry.Action` | string | no | Entry action. Allowed values: Submit, Update. Default: `Submit`. |
| `Entry.Role` | string | no | Entry role. Allowed values: Public, Internal, Reviewer. Default: `Reviewer`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entry": {
        "action": "string",
        "dateCreated": "2026-05-07T12:00:00.000Z",
        "dateUpdated": "2026-05-07T12:00:00.000Z",
        "role": "string",
        "status": "string"
      },
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entry` | object | Entry metadata and links. |
| `entry.action` | string | Entry action: Submit or Update. |
| `entry.dateCreated` | date | Entry created timestamp. |
| `entry.dateUpdated` | date | Entry updated timestamp. |
| `entry.role` | string | Entry role: Public, Internal, Reviewer. |
| `entry.status` | string | Entry status. |
| `id` | string | The Entry ID. |

## Native endpoint

Through the native Cognito Forms API, this operation is `POST /forms/:formId/entries` (base URL `https://www.cognitoforms.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-reviewer-entry.md) for the provider-specific parameters and requirements.

