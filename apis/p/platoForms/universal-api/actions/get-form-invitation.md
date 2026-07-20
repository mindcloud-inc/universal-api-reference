# PlatoForms: Get Form Invitation

Retrieves form invitation details from PlatoForms.

```
GET https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/get-form-invitation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PlatoForms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/get-form-invitation?connectionId=$CONNECTION_ID&form_identifier=string&invitation_identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "form_identifier": "string",
  "invitation_identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/get-form-invitation?${params}`, {
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
| `form_identifier` | string | yes |  |
| `invitation_identifier` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "default_prefilled_as_hidden": true,
      "default_prefilled_as_readonly": true,
      "email_invitation": {},
      "expired_unavailable_url": "https://example.com",
      "form_auto_saved": true,
      "form_available_at": "2026-05-07T12:00:00.000Z",
      "form_expired_at": "2026-05-07T12:00:00.000Z",
      "form_password_protected": true,
      "form_submit_once": true,
      "form_submitted_unavailable_url": "https://example.com",
      "id": "string",
      "invitation_name": "Ava Chen",
      "invitation_url_list": {},
      "invitation_url_number": 1,
      "is_tracking_invitation": true,
      "prefilled_data": [
        {}
      ],
      "prefilled_field_state": [
        {}
      ],
      "unavailable_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `default_prefilled_as_hidden` | boolean |  |
| `default_prefilled_as_readonly` | boolean |  |
| `email_invitation` | object |  |
| `expired_unavailable_url` | string |  |
| `form_auto_saved` | boolean |  |
| `form_available_at` | date |  |
| `form_expired_at` | date |  |
| `form_password_protected` | boolean |  |
| `form_submit_once` | boolean |  |
| `form_submitted_unavailable_url` | string |  |
| `id` | string |  |
| `invitation_name` | string |  |
| `invitation_url_list` | object |  |
| `invitation_url_number` | number |  |
| `is_tracking_invitation` | boolean |  |
| `prefilled_data` | array<object> |  |
| `prefilled_field_state` | array<object> |  |
| `unavailable_url` | string |  |

## Native endpoint

Through the native PlatoForms API, this operation is `GET /invitation/prefill/form/{{form_identifier}}/{{invitation_identifier}}/` (base URL `https://api.platoforms.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form-invitation.md) for the provider-specific parameters and requirements.

