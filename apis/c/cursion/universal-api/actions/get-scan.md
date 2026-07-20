# Cursion: Get Scan

Retrieves an existing scan from Cursion.

```
GET https://connect.mindcloud.co/v1/universal/cursion/latest/actions/get-scan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cursion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cursion/latest/actions/get-scan?connectionId=$CONNECTION_ID&scanId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scanId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cursion/latest/actions/get-scan?${params}`, {
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
| `scanId` | string | yes | The scan identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "configs": {},
      "html": "string",
      "id": "string",
      "images": [
        {}
      ],
      "lighthouse": {},
      "logs": [
        {}
      ],
      "page": "string",
      "paired_scan": "string",
      "score": 1,
      "site": "string",
      "tags": [
        "string"
      ],
      "time_completed": "string",
      "time_created": "string",
      "type": [
        "string"
      ],
      "yellowlab": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `configs` | object |  |
| `html` | string |  |
| `id` | string |  |
| `images` | array<object> |  |
| `lighthouse` | object |  |
| `logs` | array<object> |  |
| `page` | string |  |
| `paired_scan` | string |  |
| `score` | number |  |
| `site` | string |  |
| `tags` | array<string> |  |
| `time_completed` | string |  |
| `time_created` | string |  |
| `type` | array<string> |  |
| `yellowlab` | object |  |

## Native endpoint

Through the native Cursion API, this operation is `GET /scan/{{scanId}}` (base URL `https://api.cursion.dev/v1/ops`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-scan.md) for the provider-specific parameters and requirements.

