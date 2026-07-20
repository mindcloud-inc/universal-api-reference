# Sendible: List Media



```
GET https://connect.mindcloud.co/v1/universal/sendible/latest/actions/list-media
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendible `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendible/latest/actions/list-media?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendible/latest/actions/list-media?${params}`, {
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
| `mediaLibraryId` | string | no | Optional media library filter. |
| `name` | string | no | Optional media name filter. |
| `perPage` | number | no | Number of media records per page. |
| `status` | string | no | Comma-separated media statuses to include. Default: `Ready,Uploaded,Processing,New`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "paging": {},
      "result": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `paging` | object |  |
| `result` | array<object> |  |

## Native endpoint

Through the native Sendible API, this operation is `GET 0.2/tw/media` (base URL `https://api.sendible.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-media.md) for the provider-specific parameters and requirements.

