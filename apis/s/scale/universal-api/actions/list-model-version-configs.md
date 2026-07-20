# Scale: List Model Version Configs



```
GET https://connect.mindcloud.co/v1/universal/scale/latest/actions/list-model-version-configs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scale/latest/actions/list-model-version-configs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scale/latest/actions/list-model-version-configs?${params}`, {
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
      "model_version_configs": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `model_version_configs` | array<object> | Array of model version config objects. |

## Native endpoint

Through the native Scale API, this operation is `GET /v2/model_version_configs` (base URL `https://api.scale.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-model-version-configs.md) for the provider-specific parameters and requirements.

