# LightwaveRF Lighting: Get Zone

Retrieves a zone from LightwaveRF Lighting.

```
GET https://connect.mindcloud.co/v1/universal/lightwaveRFLighting/latest/actions/get-zone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LightwaveRF Lighting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightwaveRFLighting/latest/actions/get-zone?connectionId=$CONNECTION_ID&zoneId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "zoneId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightwaveRFLighting/latest/actions/get-zone?${params}`, {
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
| `zoneId` | string | yes | The LightwaveRF zone identifier to retrieve. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native LightwaveRF Lighting API returns.

## Native endpoint

Through the native LightwaveRF Lighting API, this operation is `GET /v1/zone/{zoneId}` (base URL `https://publicapi.lightwaverf.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-zone.md) for the provider-specific parameters and requirements.

