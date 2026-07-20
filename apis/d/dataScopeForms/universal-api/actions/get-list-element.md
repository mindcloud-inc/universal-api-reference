# DataScope Forms: Get List Element

Retrieves a list element from DataScope Forms.

```
GET https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/get-list-element
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataScope Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/get-list-element?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/get-list-element?${params}`, {
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
| `metadataId` | number | no | Internal identifier of the list element to fetch. |
| `metadataType` | string | no | Internal code that identifies the target list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_id": 1,
      "attribute1": "string",
      "attribute2": "string",
      "code": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "list_id": 1,
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
| `account_id` | number | Internal identifier of the account. |
| `attribute1` | string | Custom attribute 1 of the list element. |
| `attribute2` | string | Custom attribute 2 of the list element. |
| `code` | string | Code of the list element. |
| `created_at` | date | Date when the list element was created. |
| `description` | string | Description of the list element. |
| `id` | number | Internal identifier of the list element. |
| `list_id` | number | Internal identifier of the parent list. |
| `name` | string | Name of the list element. |
| `updated_at` | date | Date when the list element was updated. |

## Native endpoint

Through the native DataScope Forms API, this operation is `GET /external/metadata_object` (base URL `https://www.mydatascope.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list-element.md) for the provider-specific parameters and requirements.

