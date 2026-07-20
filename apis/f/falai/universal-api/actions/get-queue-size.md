# fal.ai: Get Queue Size

Retrieves queue size for a fal.ai application.

```
GET https://connect.mindcloud.co/v1/universal/falai/latest/actions/get-queue-size
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a fal.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/falai/latest/actions/get-queue-size?connectionId=$CONNECTION_ID&name=Ava%20Chen&owner=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen",
  "owner": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/falai/latest/actions/get-queue-size?${params}`, {
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
| `name` | string | yes | Serverless app name. |
| `owner` | string | yes | App owner name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "queue_size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `queue_size` | number |  |

## Native endpoint

Through the native fal.ai API, this operation is `GET /serverless/apps/:owner/:name/queue` (base URL `https://api.fal.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-queue-size.md) for the provider-specific parameters and requirements.

