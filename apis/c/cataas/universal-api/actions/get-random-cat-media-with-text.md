# Cataas: Get Random Cat Media With Text



```
GET https://connect.mindcloud.co/v1/universal/cataas/latest/actions/get-random-cat-media-with-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cataas `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cataas/latest/actions/get-random-cat-media-with-text?connectionId=$CONNECTION_ID&text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cataas/latest/actions/get-random-cat-media-with-text?${params}`, {
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
| `text` | string | yes | Text to render over the random cat image. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cataas API returns.

## Native endpoint

Through the native Cataas API, this operation is `GET /cat/says/:text` (base URL `https://cataas.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-random-cat-media-with-text.md) for the provider-specific parameters and requirements.

