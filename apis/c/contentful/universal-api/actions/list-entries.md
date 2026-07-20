# Contentful: List entries



```
GET https://connect.mindcloud.co/v1/universal/contentful/latest/actions/list-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Contentful `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contentful/latest/actions/list-entries?connectionId=$CONNECTION_ID&limit=25&offset=0&spaceId=cfexampleapi&environmentId=master" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "spaceId": "cfexampleapi",
  "environmentId": "master"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contentful/latest/actions/list-entries?${params}`, {
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
| `spaceId` | string | yes | Contentful space ID to query. Example: `cfexampleapi`. |
| `environmentId` | string | yes | Contentful environment ID inside the selected space. Example: `master`. |
| `contentType` | string | no | Return only entries for a specific content type ID. Example: `blogPost`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `locale` | string | no | Locale code used to localize entry fields. Example: `en-US`. |
| `include` | number | no | Linked-entry include depth from 0 to 10. Example: `1`. |
| `select` | string | no | Comma-separated list of fields to include in the response. Example: `fields.title,sys.id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "sys": {
            "id": "string",
            "type": "string"
          }
        }
      ],
      "limit": 1,
      "skip": 1,
      "sys": {
        "type": "string"
      },
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[].sys.id` | string |  |
| `items[].sys.type` | string |  |
| `limit` | number |  |
| `skip` | number |  |
| `sys.type` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Contentful API, this operation is `GET /spaces/:spaceId/environments/:environmentId/entries` (base URL `https://api.contentful.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-entries.md) for the provider-specific parameters and requirements.

