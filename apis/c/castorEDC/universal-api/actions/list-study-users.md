# Castor EDC: List Study Users

Retrieves study users from Castor EDC by study ID.

```
GET https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/list-study-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Castor EDC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/list-study-users?connectionId=$CONNECTION_ID&study_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "study_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/list-study-users?${params}`, {
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
| `study_id` | string | yes | The ID of the study for which this call should be made |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {
        "self": {
          "href": "https://example.com"
        }
      },
      "email_address": "ava@example.com",
      "entity_id": "string",
      "full_name": "Ava Chen",
      "id": "string",
      "last_login": "string",
      "manage_permissions": {
        "manage_encryption": true,
        "manage_form": true,
        "manage_records": true,
        "manage_settings": true,
        "manage_users": true
      },
      "name_first": "Ava Chen",
      "name_last": "Ava Chen",
      "role_assignments": [
        {
          "permissions": {
            "add": true,
            "catalyst_upload": true,
            "decrypt": true,
            "delete": true,
            "edit": true,
            "email_addresses": true,
            "encrypt": true,
            "export": true,
            "lock": true,
            "query": true,
            "randomization_read": true,
            "randomization_write": true,
            "sdv": true,
            "sign": true,
            "survey_send": true,
            "survey_view": true,
            "televisit": true,
            "validation": true,
            "view": true
          },
          "role_id": 1,
          "role_name": "Ava Chen",
          "site_id": "string"
        }
      ],
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links.self.href` | string |  |
| `email_address` | string |  |
| `entity_id` | string |  |
| `full_name` | string |  |
| `id` | string |  |
| `last_login` | string |  |
| `manage_permissions.manage_encryption` | boolean |  |
| `manage_permissions.manage_form` | boolean |  |
| `manage_permissions.manage_records` | boolean |  |
| `manage_permissions.manage_settings` | boolean |  |
| `manage_permissions.manage_users` | boolean |  |
| `name_first` | string |  |
| `name_last` | string |  |
| `role_assignments[].permissions.add` | boolean |  |
| `role_assignments[].permissions.catalyst_upload` | boolean |  |
| `role_assignments[].permissions.decrypt` | boolean |  |
| `role_assignments[].permissions.delete` | boolean |  |
| `role_assignments[].permissions.edit` | boolean |  |
| `role_assignments[].permissions.email_addresses` | boolean |  |
| `role_assignments[].permissions.encrypt` | boolean |  |
| `role_assignments[].permissions.export` | boolean |  |
| `role_assignments[].permissions.lock` | boolean |  |
| `role_assignments[].permissions.query` | boolean |  |
| `role_assignments[].permissions.randomization_read` | boolean |  |
| `role_assignments[].permissions.randomization_write` | boolean |  |
| `role_assignments[].permissions.sdv` | boolean |  |
| `role_assignments[].permissions.sign` | boolean |  |
| `role_assignments[].permissions.survey_send` | boolean |  |
| `role_assignments[].permissions.survey_view` | boolean |  |
| `role_assignments[].permissions.televisit` | boolean |  |
| `role_assignments[].permissions.validation` | boolean |  |
| `role_assignments[].permissions.view` | boolean |  |
| `role_assignments[].role_id` | number |  |
| `role_assignments[].role_name` | string |  |
| `role_assignments[].site_id` | string |  |
| `user_id` | string |  |

## Native endpoint

Through the native Castor EDC API, this operation is `GET /study/:study_id/user` (base URL `https://us.castoredc.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-study-users.md) for the provider-specific parameters and requirements.

