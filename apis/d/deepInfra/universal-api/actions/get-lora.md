# Deep Infra: Get LoRA



```
GET https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-lora
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deep Infra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-lora?connectionId=$CONNECTION_ID&loraName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "loraName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-lora?${params}`, {
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
| `loraName` | string | yes | LoRA adapter name from the LoRA URL path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "base_model": "string",
      "created_at": "string",
      "display_name": "Ava Chen",
      "name": "Ava Chen",
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
| `base_model` | string | Base model for the adapter. |
| `created_at` | string | Creation timestamp when returned. |
| `display_name` | string | LoRA adapter display name. |
| `name` | string | LoRA adapter name. |
| `status` | string | LoRA adapter status. |
| `updated_at` | string | Update timestamp when returned. |

## Native endpoint

Through the native Deep Infra API, this operation is `GET /v1/lora/:lora_name` (base URL `https://api.deepinfra.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lora.md) for the provider-specific parameters and requirements.

