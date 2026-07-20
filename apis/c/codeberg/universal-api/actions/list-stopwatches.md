# Codeberg: List Stopwatches



```
GET https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/list-stopwatches
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codeberg `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/list-stopwatches?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/list-stopwatches?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "duration": "string",
      "issue_index": 1,
      "issue_title": "string",
      "repo_name": "Ava Chen",
      "repo_owner_name": "Ava Chen",
      "seconds": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `duration` | string |  |
| `issue_index` | number |  |
| `issue_title` | string |  |
| `repo_name` | string |  |
| `repo_owner_name` | string |  |
| `seconds` | number |  |

## Native endpoint

Through the native Codeberg API, this operation is `GET /user/stopwatches` (base URL `https://codeberg.org/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-stopwatches.md) for the provider-specific parameters and requirements.

