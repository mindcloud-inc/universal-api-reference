# Cursion: Get Lean Test

Retrieves abbreviated test details from Cursion.

```
GET https://connect.mindcloud.co/v1/universal/cursion/latest/actions/get-lean-test
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cursion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cursion/latest/actions/get-lean-test?connectionId=$CONNECTION_ID&testId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "testId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cursion/latest/actions/get-lean-test?${params}`, {
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
| `testId` | string | yes | The test identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "images_delta": {},
      "lighthouse_delta": {},
      "page": "string",
      "post_scan": "string",
      "pre_scan": "string",
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
      "yellowlab_delta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `images_delta` | object |  |
| `lighthouse_delta` | object |  |
| `page` | string |  |
| `post_scan` | string |  |
| `pre_scan` | string |  |
| `score` | number |  |
| `site` | string |  |
| `tags` | array<string> |  |
| `time_completed` | string |  |
| `time_created` | string |  |
| `type` | array<string> |  |
| `yellowlab_delta` | object |  |

## Native endpoint

Through the native Cursion API, this operation is `GET /test/{{testId}}/lean` (base URL `https://api.cursion.dev/v1/ops`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lean-test.md) for the provider-specific parameters and requirements.

