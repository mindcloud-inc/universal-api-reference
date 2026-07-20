# Formstack Documents: Get Data Route

Retrieves data route details from Formstack Documents.

```
GET https://connect.mindcloud.co/v1/universal/formstackDocuments/latest/actions/get-data-route
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formstack Documents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formstackDocuments/latest/actions/get-data-route?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formstackDocuments/latest/actions/get-data-route?${params}`, {
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
      "id": "string",
      "key": "string",
      "name": "Ava Chen",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `key` | string |  |
| `name` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Formstack Documents API, this operation is `GET /routes/:id` (base URL `https://www.webmerge.me/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-data-route.md) for the provider-specific parameters and requirements.

