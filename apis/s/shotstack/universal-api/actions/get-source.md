# Shotstack: Get Source



```
GET https://connect.mindcloud.co/v1/universal/shotstack/latest/actions/get-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shotstack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shotstack/latest/actions/get-source?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shotstack/latest/actions/get-source?${params}`, {
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
| `id` | string | yes | The Shotstack source ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "attributes": {
          "duration": 1,
          "fps": 1,
          "height": 1,
          "id": "string",
          "input": "string",
          "outputs": {},
          "source": "string",
          "status": "string",
          "width": 1
        },
        "id": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.attributes.duration` | number | Source duration in seconds when available. |
| `data.attributes.fps` | number | Source frame rate when available. |
| `data.attributes.height` | number | Source height in pixels when available. |
| `data.attributes.id` | string | Source identifier from the attributes object. |
| `data.attributes.input` | string | Original source URL. |
| `data.attributes.outputs` | object | Generated output transformations for the source. |
| `data.attributes.source` | string | Resolved source file URL. |
| `data.attributes.status` | string | Current source ingestion status. |
| `data.attributes.width` | number | Source width in pixels when available. |
| `data.id` | string | Source identifier. |
| `data.type` | string | Resource type for the source. |

## Native endpoint

Through the native Shotstack API, this operation is `GET /ingest/v1/sources/:id` (base URL `https://api.shotstack.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-source.md) for the provider-specific parameters and requirements.

