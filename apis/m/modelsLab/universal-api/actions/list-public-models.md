# ModelsLab: List Public Models

Retrieves public models from ModelsLab.

```
GET https://connect.mindcloud.co/v1/universal/modelsLab/latest/actions/list-public-models
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ModelsLab `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/modelsLab/latest/actions/list-public-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/modelsLab/latest/actions/list-public-models?${params}`, {
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
      "description": "string",
      "model_id": "string",
      "model_name": "Ava Chen",
      "screenshots": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `model_id` | string |  |
| `model_name` | string |  |
| `screenshots` | string |  |
| `status` | string |  |

## Native endpoint

Through the native ModelsLab API, this operation is `POST /v4/dreambooth/model_list` (base URL `https://modelslab.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-public-models.md) for the provider-specific parameters and requirements.

