# LightwaveRF Lighting: Get Favourite

Retrieves a favourite from LightwaveRF Lighting.

```
GET https://connect.mindcloud.co/v1/universal/lightwaveRFLighting/latest/actions/get-favourite
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LightwaveRF Lighting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightwaveRFLighting/latest/actions/get-favourite?connectionId=$CONNECTION_ID&favouriteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "favouriteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightwaveRFLighting/latest/actions/get-favourite?${params}`, {
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
| `favouriteId` | string | yes | The LightwaveRF favourite identifier to retrieve. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native LightwaveRF Lighting API returns.

## Native endpoint

Through the native LightwaveRF Lighting API, this operation is `GET /v1/favourite/{favouriteId}` (base URL `https://publicapi.lightwaverf.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-favourite.md) for the provider-specific parameters and requirements.

