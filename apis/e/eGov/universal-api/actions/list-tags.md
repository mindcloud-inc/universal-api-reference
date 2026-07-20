# e-Gov: List Tags

Retrieves tags from e-Gov.

```
GET https://connect.mindcloud.co/v1/universal/eGov/latest/actions/list-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a e-Gov `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGov/latest/actions/list-tags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eGov/latest/actions/list-tags?${params}`, {
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
| `query` | string | no | Return tags whose names contain this text. |
| `all_fields` | boolean | no | Return full tag records instead of names. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `vocabulary_id` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "display_name": "Ava Chen",
      "id": "string",
      "name": "Ava Chen",
      "vocabulary_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `display_name` | string |  |
| `id` | string |  |
| `name` | string |  |
| `vocabulary_id` | string |  |

## Native endpoint

Through the native e-Gov API, this operation is `GET /tag_list` (base URL `https://data.e-gov.go.jp/data/api/action`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tags.md) for the provider-specific parameters and requirements.

