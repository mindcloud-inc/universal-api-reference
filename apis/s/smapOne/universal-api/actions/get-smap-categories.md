# smapOne: Get smap categories

Retrieves categories for a smap from smapOne.

```
GET https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/get-smap-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a smapOne `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/get-smap-categories?connectionId=$CONNECTION_ID&smap_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "smap_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/get-smap-categories?${params}`, {
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
| `smap_id` | string | yes | The smap id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assigned": true,
      "categoryId": "string",
      "id": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assigned` | boolean |  |
| `categoryId` | string |  |
| `id` | string |  |
| `title` | string |  |

## Native endpoint

Through the native smapOne API, this operation is `GET /smaps/overview/{smapId}/categories` (base URL `https://platform.smapone.com/Backend`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-smap-categories.md) for the provider-specific parameters and requirements.

