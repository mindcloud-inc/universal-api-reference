# PlatoForms: List Forms

Retrieves a list of forms from PlatoForms.

```
GET https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/list-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PlatoForms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/list-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/list-forms?${params}`, {
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
| `status` | string | no | Filter forms by status: published (default), draft, archived, or all |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_date": "2026-05-07T12:00:00.000Z",
      "current_version_submission": "string",
      "folder": {},
      "id": "string",
      "is_published": "string",
      "modified_date": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "pdf": {},
      "published_url": "https://example.com",
      "published_version": "string",
      "total_submission": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_date` | date |  |
| `current_version_submission` | string |  |
| `folder` | object |  |
| `id` | string |  |
| `is_published` | string |  |
| `modified_date` | date |  |
| `name` | string |  |
| `pdf` | object |  |
| `published_url` | string |  |
| `published_version` | string |  |
| `total_submission` | string |  |

## Native endpoint

Through the native PlatoForms API, this operation is `GET /forms/` (base URL `https://api.platoforms.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-forms.md) for the provider-specific parameters and requirements.

