# CAMB.AI: Get Translation Result

Retrieves a translation result from CAMB.AI.

```
GET https://connect.mindcloud.co/v1/universal/cAMBAI/latest/actions/get-translation-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CAMB.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cAMBAI/latest/actions/get-translation-result?connectionId=$CONNECTION_ID&run_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "run_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cAMBAI/latest/actions/get-translation-result?${params}`, {
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
| `run_id` | number | yes | Run identifier returned by a completed translation task. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "texts": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `texts` | array<string> | Translated text segments in the same order as the input. |

## Native endpoint

Through the native CAMB.AI API, this operation is `GET /translation-result/:run_id` (base URL `https://client.camb.ai/apis`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-translation-result.md) for the provider-specific parameters and requirements.

