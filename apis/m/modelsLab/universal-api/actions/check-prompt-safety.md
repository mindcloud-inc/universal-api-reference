# ModelsLab: Check Prompt Safety

Checks a prompt for safety issues in ModelsLab.

```
GET https://connect.mindcloud.co/v1/universal/modelsLab/latest/actions/check-prompt-safety
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ModelsLab `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/modelsLab/latest/actions/check-prompt-safety?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/modelsLab/latest/actions/check-prompt-safety?${params}`, {
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
| `prompt` | string | no | Prompt text to check for NSFW or CP content. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "filtered_prompt": "string",
      "is_cp": true,
      "is_nsfw": true,
      "original_prompt": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `filtered_prompt` | string |  |
| `is_cp` | boolean |  |
| `is_nsfw` | boolean |  |
| `original_prompt` | string |  |
| `status` | string |  |

## Native endpoint

Through the native ModelsLab API, this operation is `POST /check_nsfw_cp` (base URL `https://modelslab.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-prompt-safety.md) for the provider-specific parameters and requirements.

