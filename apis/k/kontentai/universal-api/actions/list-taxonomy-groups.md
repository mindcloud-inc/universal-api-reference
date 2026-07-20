# Kontent.ai: List taxonomy groups

Retrieves taxonomy groups from your Kontent.ai environment.

```
GET https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/list-taxonomy-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kontent.ai `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/list-taxonomy-groups?connectionId=$CONNECTION_ID&limit=25&offset=0&environmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "environmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/list-taxonomy-groups?${params}`, {
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
      "id": "string",
      "name": "Ava Chen",
      "terms": [
        {
          "codename": "Ava Chen",
          "id": "string",
          "name": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `codename` | string | Taxonomy group codename. |
| `id` | string | Taxonomy group ID. |
| `name` | string | Taxonomy group name. |
| `terms[].codename` | string | Taxonomy term codename. |
| `terms[].id` | string | Taxonomy term ID. |
| `terms[].name` | string | Taxonomy term name. |

## Native endpoint

Through the native Kontent.ai API, this operation is `GET /:environment_id/taxonomies` (base URL `https://deliver.kontent.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-taxonomy-groups.md) for the provider-specific parameters and requirements.

