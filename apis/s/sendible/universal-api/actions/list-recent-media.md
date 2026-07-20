# Sendible: List Recent Media



```
GET https://connect.mindcloud.co/v1/universal/sendible/latest/actions/list-recent-media
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendible `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendible/latest/actions/list-recent-media?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendible/latest/actions/list-recent-media?${params}`, {
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
| `filter` | string | no | Optional recent media filter value. |
| `perPage` | number | no | Number of results per page. Default: `30`. |
| `userIds` | string | no | Optional comma-separated user IDs to filter recent media. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "files": [
        {}
      ],
      "pageCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `files` | array<object> |  |
| `pageCount` | number |  |

## Native endpoint

Through the native Sendible API, this operation is `GET api/v2/media.json` (base URL `https://api.sendible.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-recent-media.md) for the provider-specific parameters and requirements.

