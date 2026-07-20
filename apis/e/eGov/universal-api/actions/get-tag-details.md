# e-Gov: Get Tag Details

Retrieves a tag and its datasets from e-Gov.

```
GET https://connect.mindcloud.co/v1/universal/eGov/latest/actions/get-tag-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a e-Gov `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGov/latest/actions/get-tag-details?connectionId=$CONNECTION_ID&id=%E4%BA%A4%E9%80%9A%E4%BA%8B%E6%95%85%E7%B5%B1%E8%A8%88" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "交通事故統計"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eGov/latest/actions/get-tag-details?${params}`, {
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
| `id` | string | yes | Default: `交通事故統計`. |

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

Through the native e-Gov API, this operation is `GET /tag_show` (base URL `https://data.e-gov.go.jp/data/api/action`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tag-details.md) for the provider-specific parameters and requirements.

