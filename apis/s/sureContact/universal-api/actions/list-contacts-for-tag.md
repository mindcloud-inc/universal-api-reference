# SureContact: List Contacts for Tag

Retrieves contacts assigned to a SureContact tag.

```
GET https://connect.mindcloud.co/v1/universal/sureContact/latest/actions/list-contacts-for-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SureContact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sureContact/latest/actions/list-contacts-for-tag?connectionId=$CONNECTION_ID&tagUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tagUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sureContact/latest/actions/list-contacts-for-tag?${params}`, {
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
| `perPage` | number | no |  |
| `tagUuid` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "do_not_email": true,
      "email": "ava@example.com",
      "email_status": "ava@example.com",
      "first_name": "Ava",
      "formal_name": "Ava Chen",
      "full_name": "Ava Chen",
      "job_title": "string",
      "language": "string",
      "last_activity_at": "2026-05-07T12:00:00.000Z",
      "last_name": "Chen",
      "source": "string",
      "source_label": "string",
      "status": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string |  |
| `created_at` | date |  |
| `do_not_email` | boolean |  |
| `email` | string |  |
| `email_status` | string |  |
| `first_name` | string |  |
| `formal_name` | string |  |
| `full_name` | string |  |
| `job_title` | string |  |
| `language` | string |  |
| `last_activity_at` | date |  |
| `last_name` | string |  |
| `source` | string |  |
| `source_label` | string |  |
| `status` | string |  |
| `updated_at` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native SureContact API, this operation is `GET api/v1/public/tags/:tag_uuid/contacts` (base URL `https://api.surecontact.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts-for-tag.md) for the provider-specific parameters and requirements.

