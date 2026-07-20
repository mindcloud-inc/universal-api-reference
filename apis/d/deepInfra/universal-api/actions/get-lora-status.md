# Deep Infra: Get LoRA Status



```
GET https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-lora-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deep Infra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-lora-status?connectionId=$CONNECTION_ID&loraName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "loraName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-lora-status?${params}`, {
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
| `loraName` | string | yes | LoRA adapter name from the LoRA status URL path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "name": "Ava Chen",
      "progress": 1,
      "status": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider status message. |
| `name` | string | LoRA adapter name. |
| `progress` | number | Processing progress when returned. |
| `status` | string | LoRA processing status. |
| `updated_at` | string | Status update timestamp when returned. |

## Native endpoint

Through the native Deep Infra API, this operation is `GET /v1/lora/:lora_name/status` (base URL `https://api.deepinfra.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lora-status.md) for the provider-specific parameters and requirements.

