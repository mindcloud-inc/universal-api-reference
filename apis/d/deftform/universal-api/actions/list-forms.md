# Deftform: List Forms

Retrieves forms and fields from Deftform.

```
GET https://connect.mindcloud.co/v1/universal/deftform/latest/actions/list-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deftform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deftform/latest/actions/list-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deftform/latest/actions/list-forms?${params}`, {
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
      "after_redirect_url": "https://example.com",
      "captcha": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "cta_label": "string",
      "description": "string",
      "fields": [
        {}
      ],
      "id": "string",
      "is_closed": true,
      "name": "Ava Chen",
      "seo_description": "string",
      "seo_title": "string",
      "show_formtitle": true,
      "slug": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `after_message` | string | Message shown after submission or null. |
| `after_redirect_url` | string | Redirect URL after submission or null. |
| `captcha` | string | CAPTCHA setting or null. |
| `created_at` | date | Form creation timestamp. |
| `cta_label` | string | Call-to-action label or null. |
| `description` | string | Form description or null. |
| `fields` | array<object> | Fields belonging to the form. |
| `id` | string | Form ID returned by Deftform. |
| `is_closed` | boolean | Whether the form is closed. |
| `name` | string | Form name. |
| `seo_description` | string | SEO description or null. |
| `seo_title` | string | SEO title or null. |
| `show_formtitle` | boolean | Whether the form title is shown. |
| `slug` | string | Public form slug. |
| `updated_at` | date | Form update timestamp. |

## Native endpoint

Through the native Deftform API, this operation is `GET /forms` (base URL `https://deftform.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-forms.md) for the provider-specific parameters and requirements.

