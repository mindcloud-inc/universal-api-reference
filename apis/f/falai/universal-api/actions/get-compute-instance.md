# fal.ai: Get Compute Instance

Retrieves compute instance details from fal.ai.

```
GET https://connect.mindcloud.co/v1/universal/falai/latest/actions/get-compute-instance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a fal.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/falai/latest/actions/get-compute-instance?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/falai/latest/actions/get-compute-instance?${params}`, {
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
| `id` | string | yes | Compute instance identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creator_user_nickname": "Ava Chen",
      "id": "string",
      "instance_type": "string",
      "ip": "string",
      "region": "string",
      "sector": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creator_user_nickname` | string |  |
| `id` | string |  |
| `instance_type` | string |  |
| `ip` | string |  |
| `region` | string |  |
| `sector` | string |  |
| `status` | string |  |

## Native endpoint

Through the native fal.ai API, this operation is `GET /compute/instances/:id` (base URL `https://api.fal.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-compute-instance.md) for the provider-specific parameters and requirements.

