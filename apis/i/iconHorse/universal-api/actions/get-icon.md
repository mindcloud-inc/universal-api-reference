# Icon Horse: Get Icon

Retrieves a website icon from Icon Horse by hostname.

```
GET https://connect.mindcloud.co/v1/universal/iconHorse/latest/actions/get-icon
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Icon Horse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iconHorse/latest/actions/get-icon?connectionId=$CONNECTION_ID&hostname=github.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "hostname": "github.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iconHorse/latest/actions/get-icon?${params}`, {
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
| `hostname` | string | yes | Fully qualified domain name such as github.com, wikipedia.org, or youtube.com. Default: `github.com`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Icon Horse API returns.

## Native endpoint

Through the native Icon Horse API, this operation is `GET /icon/:hostname` (base URL `https://icon.horse`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-icon.md) for the provider-specific parameters and requirements.

