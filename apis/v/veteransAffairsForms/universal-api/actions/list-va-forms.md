# Veterans Affairs Forms: List VA Forms

Finds VA forms by number, keyword, or title.

```
GET https://connect.mindcloud.co/v1/universal/veteransAffairsForms/latest/actions/list-va-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veterans Affairs Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veteransAffairsForms/latest/actions/list-va-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veteransAffairsForms/latest/actions/list-va-forms?${params}`, {
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
| `query` | string | no | Optional form number, keyword, or title used to filter VA forms. Example: `10-10EZ or health benefits`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "benefit_categories": [
          {}
        ],
        "deleted_at": "2026-05-07T12:00:00.000Z",
        "first_issued_on": "2026-05-07T12:00:00.000Z",
        "form_details_url": "https://example.com",
        "form_name": "Ava Chen",
        "form_tool_intro": "string",
        "form_tool_url": "https://example.com",
        "form_type": "string",
        "form_usage": "string",
        "language": "string",
        "last_revision_on": "2026-05-07T12:00:00.000Z",
        "last_sha256_change": "2026-05-07T12:00:00.000Z",
        "pages": 1,
        "related_forms": [
          "string"
        ],
        "sha256": "string",
        "title": "string",
        "url": "https://example.com",
        "va_form_administration": "string",
        "valid_pdf": true
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.benefit_categories` | array<object> | Benefit categories related to the form. |
| `attributes.deleted_at` | date | Deletion timestamp when VA has removed the form. |
| `attributes.first_issued_on` | date | Date the form first became available. |
| `attributes.form_details_url` | string | VA.gov details page URL, when available. |
| `attributes.form_name` | string | VA form name, such as 10-10EZ. |
| `attributes.form_tool_intro` | string | Introductory text for an online tool, when available. |
| `attributes.form_tool_url` | string | Online tool URL, when available. |
| `attributes.form_type` | string | VA form type. |
| `attributes.form_usage` | string | Description of how the form is used. |
| `attributes.language` | string | Language code. |
| `attributes.last_revision_on` | date | Date the form was last revised. |
| `attributes.last_sha256_change` | date | Date of the last SHA256 hash change. |
| `attributes.pages` | number | Number of pages. |
| `attributes.related_forms` | array<string> | Related VA form names. |
| `attributes.sha256` | string | SHA256 hash for the form PDF. |
| `attributes.title` | string | VA form title. |
| `attributes.url` | string | PDF URL for the form when published. |
| `attributes.va_form_administration` | string | VA organization administering the form. |
| `attributes.valid_pdf` | boolean | Whether the PDF URL was confirmed valid. |
| `id` | string | JSON API identifier. |
| `type` | string | JSON API resource type. |

## Native endpoint

Through the native Veterans Affairs Forms API, this operation is `GET /forms` (base URL `https://sandbox-api.va.gov/services/va_forms/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-va-forms.md) for the provider-specific parameters and requirements.

