# Stackoverflow: List Tag Synonyms

Retrieves tag synonyms for specific tags from Stackoverflow.

```
GET https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/list-tag-synonyms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stackoverflow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/list-tag-synonyms?connectionId=$CONNECTION_ID&limit=25&offset=0&tags=string&site=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "tags": "string",
  "site": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/list-tag-synonyms?${params}`, {
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
| `tags` | string | yes | Semicolon-delimited tag names. |
| `site` | string | yes | API site parameter, for example stackoverflow. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applied_count": 1,
      "creation_date": "2026-05-07T12:00:00.000Z",
      "from_tag": "string",
      "last_applied_date": "2026-05-07T12:00:00.000Z",
      "to_tag": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applied_count` | number |  |
| `creation_date` | date |  |
| `from_tag` | string |  |
| `last_applied_date` | date |  |
| `to_tag` | string |  |

## Native endpoint

Through the native Stackoverflow API, this operation is `GET /tags/[:tags]/synonyms` (base URL `https://api.stackexchange.com/2.3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tag-synonyms.md) for the provider-specific parameters and requirements.

