# Oneflow: List Contacts

Retrieves contacts from Oneflow.

```
GET https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Oneflow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0&workspaceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "workspaceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/list-contacts?${params}`, {
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
| `workspaceId` | number | yes | The Oneflow workspace ID whose contacts should be listed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company_name": "Ava Chen",
      "company_registration_number": "string",
      "country_code": "string",
      "created_time": "string",
      "date_of_birth": "string",
      "email": "ava@example.com",
      "id": 1,
      "name": "Ava Chen",
      "notes": "string",
      "phone_number": "string",
      "title": "string",
      "updated_time": "string",
      "workspace_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company_name` | string | The name of the contact person's company. |
| `company_registration_number` | string | The registration number of the contact person's company. |
| `country_code` | string | The country code of the contact. |
| `created_time` | string | The time the contact was created. |
| `date_of_birth` | string | The date of birth of the contact person. |
| `email` | string | The email of the contact person. |
| `id` | number | The ID of the contact. |
| `name` | string | The name of the contact person. |
| `notes` | string | Notes added to the contact. |
| `phone_number` | string | The phone number of the contact person. |
| `title` | string | The title of the contact person. |
| `updated_time` | string | The time the contact was last updated. |
| `workspace_id` | number | The workspace ID the contact belongs to. |

## Native endpoint

Through the native Oneflow API, this operation is `GET /contacts` (base URL `https://api.oneflow.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

