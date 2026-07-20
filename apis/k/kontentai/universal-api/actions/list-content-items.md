# Kontent.ai: List content items

Retrieves content items from your Kontent.ai environment.

```
GET https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/list-content-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kontent.ai `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/list-content-items?connectionId=$CONNECTION_ID&limit=25&offset=0&environmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "environmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/list-content-items?${params}`, {
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
| `language` | string | no | Language codename used to localize returned content. Example: `en-US`. |
| `depth` | number | no | How many levels of linked content to include. Example: `1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `elements` | string | no | Comma-separated element codenames to include. Accepts multiple values in one string, delimited by `,`. |
| `excludeElements` | string | no | Comma-separated element codenames to exclude. Accepts multiple values in one string, delimited by `,`. |
| `systemType` | string | no | Filter content items by content type codename. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "elements": {},
      "system": {
        "codename": "Ava Chen",
        "collection": "string",
        "id": "string",
        "language": "string",
        "last_modified": "2026-05-07T12:00:00.000Z",
        "name": "Ava Chen",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `elements` | object | Content item element values. |
| `system.codename` | string | Content item codename. |
| `system.collection` | string | Collection codename. |
| `system.id` | string | Content item system ID. |
| `system.language` | string | Language codename. |
| `system.last_modified` | date | Last modified timestamp. |
| `system.name` | string | Content item display name. |
| `system.type` | string | Content type codename. |

## Native endpoint

Through the native Kontent.ai API, this operation is `GET /:environment_id/items` (base URL `https://deliver.kontent.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-content-items.md) for the provider-specific parameters and requirements.

