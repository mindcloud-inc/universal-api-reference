# KLIPY: Search Memes

Finds memes in KLIPY by search term.

```
GET https://connect.mindcloud.co/v1/universal/kLIPY/latest/actions/search-memes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KLIPY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kLIPY/latest/actions/search-memes?connectionId=$CONNECTION_ID&customerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kLIPY/latest/actions/search-memes?${params}`, {
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
| `contentFilter` | string | no |  |
| `customerId` | string | yes |  |
| `formatFilter` | string | no |  |
| `locale` | string | no |  |
| `page` | string | no |  |
| `perPage` | string | no |  |
| `query` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native KLIPY API returns.

## Native endpoint

Through the native KLIPY API, this operation is `GET /api/v1/:app_key/static-memes/search` (base URL `https://api.klipy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-memes.md) for the provider-specific parameters and requirements.

