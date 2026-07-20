# Kontent.ai: List content types

Retrieves content types from your Kontent.ai environment.

```
GET https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/list-content-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kontent.ai `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/list-content-types?connectionId=$CONNECTION_ID&limit=25&offset=0&environmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "environmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/list-content-types?${params}`, {
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
| `environmentId` | string | yes | Kontent.ai project environment identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "codename": "Ava Chen",
      "elements": [
        {
          "codename": "Ava Chen",
          "id": "string",
          "name": "Ava Chen",
          "type": "string"
        }
      ],
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `codename` | string | Content type codename. |
| `elements[].codename` | string | Element codename. |
| `elements[].id` | string | Element ID. |
| `elements[].name` | string | Element name. |
| `elements[].type` | string | Element type. |
| `id` | string | Content type ID. |
| `name` | string | Content type name. |

## Native endpoint

Through the native Kontent.ai API, this operation is `GET /:environment_id/types` (base URL `https://deliver.kontent.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-content-types.md) for the provider-specific parameters and requirements.

