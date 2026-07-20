# Deep Infra: List User LoRAs



```
GET https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/list-user-loras
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deep Infra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/list-user-loras?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/list-user-loras?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `base_model` | string | Base model for the LoRA adapter. |
| `created_at` | string | Creation timestamp when returned. |
| `display_name` | string | User LoRA display name. |
| `name` | string | User LoRA adapter name. |
| `status` | string | LoRA adapter status. |

## Native endpoint

Through the native Deep Infra API, this operation is `GET /v1/user/loras` (base URL `https://api.deepinfra.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-loras.md) for the provider-specific parameters and requirements.

