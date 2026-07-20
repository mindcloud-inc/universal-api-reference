# Leadspicker: List API Changelog Entries

Retrieves API changelog entries from Leadspicker.

```
GET https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/list-api-changelog-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadspicker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/list-api-changelog-entries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/list-api-changelog-entries?${params}`, {
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
      "affected_endpoints": [
        "string"
      ],
      "change_type": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "effective_at": "2026-05-07T12:00:00.000Z",
      "is_breaking": true,
      "title": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affected_endpoints` | array<string> |  |
| `change_type` | string |  |
| `date` | date |  |
| `description` | string |  |
| `effective_at` | date |  |
| `is_breaking` | boolean |  |
| `title` | string |  |
| `version` | string |  |

## Native endpoint

Through the native Leadspicker API, this operation is `GET /app/sb/api/api-changelog` (base URL `https://app.leadspicker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-api-changelog-entries.md) for the provider-specific parameters and requirements.

