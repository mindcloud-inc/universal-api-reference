# Formstack: Create Form

Creates a new form in Formstack.

```
POST https://connect.mindcloud.co/v1/universal/formstack/latest/actions/create-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formstack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formstack/latest/actions/create-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formstack/latest/actions/create-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Name of the form. Example: `Customer Intake Form`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `template` | number | no | ID of template of the form. Example: `123456`. |
| `stockTemplate` | list<string> | no | Stock theme template code for the form. One of: `berryNice`, `blueAfterglow`, `calmZigZag`, `celadonParchment`, `clean`, `confetti`, `corporateOffice`, `dark`, `duskPop`, `formstack`, `geometric`, `light`, `midnight`, `minimalism`, `oceanTide`, `peachyKeen`, `simple`. |
| `folder` | number | no | ID of the folder where the form will be created. Example: `123456`. |
| `submitButtonTitle` | string | no | Title of submit button on live form. Example: `Submit Form`. |
| `numberOfColumns` | number | no | Number of visible columns in the form. Example: `1`. |
| `fieldLabelsPosition` | list<string> | no | Position where field labels are placed on the live form. One of: `left`, `top`. |
| `saveSubmissionsToDatabase` | boolean | no | Flag to disable or enable submissions to be saved in the database. |
| `timezone` | string | no | Timezone of the form. Example: `US/Eastern`. |
| `language` | string | no | Language of the form. Example: `en`. |
| `isActive` | boolean | no | Flag to make the form active or inactive. |
| `disabledMessage` | string | no | Message to show when the form is inactive. Example: `This form is currently unavailable.`. |
| `fields[]` | array<object> | no | Optional fields to create with the form as raw Create Field objects. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canEdit": true,
      "created": "2026-05-07T12:00:00.000Z",
      "fields": [
        {}
      ],
      "folder": 1,
      "formExtras": {},
      "formSettings": {},
      "hasApprovers": true,
      "id": 1,
      "isEncrypted": true,
      "isWorkflowForm": true,
      "isWorkflowPublished": true,
      "name": "Ava Chen",
      "permissions": 1,
      "submissionsCount": 1,
      "submitButtonTitle": "string",
      "todaySubmissionsCount": 1,
      "unreadSubmissionsCount": 1,
      "updated": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "version": 1,
      "viewKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canEdit` | boolean | Whether the user can edit this form. |
| `created` | date | Date when the form was created. |
| `fields` | array<object> | Form fields included in the response. |
| `folder` | number | ID of the folder where the form is located. |
| `formExtras` | object | Form extras response. |
| `formSettings` | object | Form settings response. |
| `hasApprovers` | boolean | Whether this form has approvers configured. |
| `id` | number | The ID of the form. |
| `isEncrypted` | boolean | Whether the form is encrypted. |
| `isWorkflowForm` | boolean | Whether this form is a workflow form. |
| `isWorkflowPublished` | boolean | Whether this workflow is published. |
| `name` | string | Name of the form. |
| `permissions` | number | User permission level for this form. |
| `submissionsCount` | number | Count of form submissions. |
| `submitButtonTitle` | string | Title of submit button on the live form. |
| `todaySubmissionsCount` | number | Count of today's form submissions. |
| `unreadSubmissionsCount` | number | Count of unread form submissions. |
| `updated` | date | Date when the form was last updated. |
| `url` | string | URL of the live form. |
| `version` | number | Version of the form. |
| `viewKey` | string | View key of the form. |

## Native endpoint

Through the native Formstack API, this operation is `POST /forms` (base URL `https://www.formstack.com/api/v2025`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-form.md) for the provider-specific parameters and requirements.

