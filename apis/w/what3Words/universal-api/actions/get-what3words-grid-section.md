# What3Words: Get what3words Grid Section

Retrieves a what3words grid section by bounding box.

```
GET https://connect.mindcloud.co/v1/universal/what3Words/latest/actions/get-what3words-grid-section
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a What3Words `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/what3Words/latest/actions/get-what3words-grid-section?connectionId=$CONNECTION_ID&boundingBox=52.207988%2C0.116126%2C52.208867%2C0.117540" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "boundingBox": "52.207988,0.116126,52.208867,0.117540"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/what3Words/latest/actions/get-what3words-grid-section?${params}`, {
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
| `boundingBox` | string | yes | Bounding box as south,west,north,east. The box must not exceed 4 km corner-to-corner. Example: `52.207988,0.116126,52.208867,0.117540`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `format` | list<string> | no | Response format: json or geojson. One of: `geojson`, `json`. Default: `json`. Example: `json`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "lines": [
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
| `lines` | array<object> | Grid line segments for the requested bounding box. |

## Native endpoint

Through the native What3Words API, this operation is `GET /grid-section` (base URL `https://api.what3words.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-what3words-grid-section.md) for the provider-specific parameters and requirements.

