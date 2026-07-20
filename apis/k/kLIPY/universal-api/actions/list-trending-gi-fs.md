# KLIPY: List Trending GIFs

Retrieves current trending GIFs from KLIPY.

```
GET https://connect.mindcloud.co/v1/universal/kLIPY/latest/actions/list-trending-gi-fs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KLIPY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kLIPY/latest/actions/list-trending-gi-fs?connectionId=$CONNECTION_ID&customerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kLIPY/latest/actions/list-trending-gi-fs?${params}`, {
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
| `page` | number | no | Default: `1`. |
| `perPage` | number | no | Default: `24`. |
| `customerId` | string | yes |  |
| `locale` | string | no |  |
| `formatFilter` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native KLIPY API returns.

## Native endpoint

Through the native KLIPY API, this operation is `GET /api/v1/:app_key/gifs/trending` (base URL `https://api.klipy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-trending-gi-fs.md) for the provider-specific parameters and requirements.

