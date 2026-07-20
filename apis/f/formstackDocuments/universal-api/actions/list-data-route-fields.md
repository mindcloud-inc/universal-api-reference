# Formstack Documents: List Data Route Fields

Retrieves data route fields from Formstack Documents.

```
GET https://connect.mindcloud.co/v1/universal/formstackDocuments/latest/actions/list-data-route-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formstack Documents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formstackDocuments/latest/actions/list-data-route-fields?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formstackDocuments/latest/actions/list-data-route-fields?${params}`, {
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
| `id` | string | yes | The data route ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "key": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `key` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Formstack Documents API, this operation is `GET /routes/:id/fields` (base URL `https://www.webmerge.me/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-data-route-fields.md) for the provider-specific parameters and requirements.

