# RealFaviconGenerator: List change log



```
GET https://connect.mindcloud.co/v1/universal/realFaviconGenerator/latest/actions/list-change-log
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RealFaviconGenerator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/realFaviconGenerator/latest/actions/list-change-log?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/realFaviconGenerator/latest/actions/list-change-log?${params}`, {
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
| `since` | string | no | Only return changes after this existing RealFaviconGenerator version, such as 0.5. Example: `0.5`. |
| `format` | list | no | Human-readable description format returned by the API. One of: `html`, `markdown`. Default: `html`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "importance": "string",
      "relevance": {},
      "updateOrNot": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date | Release date from the provider response. |
| `description` | string | Release description in the requested format. |
| `importance` | string | Provider importance label. |
| `relevance` | object | Relevance flags for automated and manual updates. |
| `updateOrNot` | string | Provider guidance about whether to update. |
| `version` | string | RealFaviconGenerator package version. |

## Native endpoint

Through the native RealFaviconGenerator API, this operation is `GET /change-log` (base URL `https://realfavicongenerator.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-change-log.md) for the provider-specific parameters and requirements.

