# Global Patron: List Form User Security Settings

Lists form user security settings in Global Patron.

```
GET https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/list-form-user-security-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Global Patron `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/list-form-user-security-settings?connectionId=$CONNECTION_ID&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/list-form-user-security-settings?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | ID of the form. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "formDocumentBasic": {
        "formName": "Ava Chen",
        "id": "string"
      },
      "grantedFormRoles": [
        "string"
      ],
      "results": [
        {
          "canEditForm": true,
          "canEditSettings": true,
          "canManageUsers": true,
          "canManageWebhooks": true,
          "canViewSubmissions": true,
          "email": "ava@example.com",
          "id": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `formDocumentBasic` | object | Basic form metadata. |
| `formDocumentBasic.formName` | string | Form name. |
| `formDocumentBasic.id` | string | Form identifier. |
| `grantedFormRoles` | array<string> | Roles granted to the current user. |
| `results` | array<object> | Users with form security settings. |
| `results[].canEditForm` | boolean | Whether the user can edit the form. |
| `results[].canEditSettings` | boolean | Whether the user can edit settings. |
| `results[].canManageUsers` | boolean | Whether the user can manage form users. |
| `results[].canManageWebhooks` | boolean | Whether the user can manage webhooks. |
| `results[].canViewSubmissions` | boolean | Whether the user can view submissions. |
| `results[].email` | string | Collaborator email address. |
| `results[].id` | string | User security record identifier. |

## Native endpoint

Through the native Global Patron API, this operation is `GET /api/restricted/form/{formId}/usersecurity` (base URL `https://api.globalpatron.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-form-user-security-settings.md) for the provider-specific parameters and requirements.

