# Deftform: Get Workspace

Retrieves your workspace details from Deftform.

```
GET https://connect.mindcloud.co/v1/universal/deftform/latest/actions/get-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deftform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deftform/latest/actions/get-workspace?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deftform/latest/actions/get-workspace?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "after_message": "string",
      "after_message_email": "ava@example.com",
      "after_message_email_subject": "ava@example.com",
      "after_redirect_url": "https://example.com",
      "altcha_label": "string",
      "altcha_label_verified": "string",
      "checkout_canceled_cta": "string",
      "checkout_canceled_message": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "favicon": "string",
      "field_errormessage": "string",
      "form_not_found_message": "string",
      "locale": "string",
      "logo": "string",
      "logo_backend": "string",
      "members": [
        {}
      ],
      "name": "Ava Chen",
      "ogimage": "string",
      "onboarding_completed": true,
      "owner": {},
      "replyto_email": "ava@example.com",
      "time_restriction_message": "string",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `after_message` | string | Default after-submission message. |
| `after_message_email` | string | Default confirmation email message or null. |
| `after_message_email_subject` | string | Default confirmation email subject or null. |
| `after_redirect_url` | string | Default post-submit redirect URL or null. |
| `altcha_label` | string | ALTCHA challenge label. |
| `altcha_label_verified` | string | ALTCHA verified-state label or null. |
| `checkout_canceled_cta` | string | Checkout canceled call-to-action label or null. |
| `checkout_canceled_message` | string | Checkout canceled message or null. |
| `created_at` | date | Workspace creation timestamp. |
| `favicon` | string | Workspace favicon URL or null. |
| `field_errormessage` | string | Default field validation error message. |
| `form_not_found_message` | string | Form-not-found message or null. |
| `locale` | string | Workspace locale. |
| `logo` | string | Workspace logo URL or null. |
| `logo_backend` | string | Backend logo URL or null. |
| `members` | array<object> | Workspace members. |
| `name` | string | Workspace name. |
| `ogimage` | string | Open graph image URL or null. |
| `onboarding_completed` | boolean | Whether workspace onboarding is complete. |
| `owner` | object | Workspace owner details. |
| `replyto_email` | string | Reply-to email address or null. |
| `time_restriction_message` | string | Time restriction message or null. |
| `timezone` | string | Workspace timezone. |

## Native endpoint

Through the native Deftform API, this operation is `GET /workspace` (base URL `https://deftform.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace.md) for the provider-specific parameters and requirements.

