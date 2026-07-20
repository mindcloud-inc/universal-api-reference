# Deftform: Update Form Settings

Updates existing form settings in Deftform.

```
PUT https://connect.mindcloud.co/v1/universal/deftform/latest/actions/update-form-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deftform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/deftform/latest/actions/update-form-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deftform/latest/actions/update-form-settings', {
  method: 'PUT',
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
| `formId` | string | yes | The Deftform form ID whose settings should be updated. |
| `name` | string | no | New form name. Maximum 255 characters. |
| `description` | string | no | Form description. Maximum 1000 characters. |
| `isClosed` | boolean | no | Whether the form is closed. |
| `responsesLimit` | number | no | Optional response limit. Minimum 1. |
| `afterMessage` | string | no | Message shown after a submission. |
| `afterRedirectUrl` | string | no | URL to redirect respondents after submission. Maximum 500 characters. |
| `ctaLabel` | string | no | Call-to-action label. Maximum 100 characters. |
| `ctaLabelContinue` | string | no | Continue button label. Maximum 100 characters. |
| `captcha` | list<string> | no | CAPTCHA provider: altcha, turnstile, recaptcha, or none. One of: `0`, `1`, `2`, `3`. |
| `showFormTitle` | boolean | no | Whether to show the form title. |
| `seoTitle` | string | no | SEO title. Maximum 255 characters. |
| `seoDescription` | string | no | SEO description. Maximum 500 characters. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Form ID. |
| `name` | string | Updated form name. |
| `updated_at` | date | Timestamp when the form settings were updated. |

## Native endpoint

Through the native Deftform API, this operation is `POST /forms/:formId/settings` (base URL `https://deftform.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-form-settings.md) for the provider-specific parameters and requirements.

