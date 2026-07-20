# Scale: Get Autoeval Model Version Config Statuses



```
GET https://connect.mindcloud.co/v1/universal/scale/latest/actions/get-autoeval-model-version-config-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scale/latest/actions/get-autoeval-model-version-config-statuses?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scale/latest/actions/get-autoeval-model-version-config-statuses?${params}`, {
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
| `id` | string | yes | The model version config identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "statuses": [
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
| `statuses` | array<object> | Array of status objects. |

## Native endpoint

Through the native Scale API, this operation is `GET /v2/autoevals/model_version_configs/{id}/statuses` (base URL `https://api.scale.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-autoeval-model-version-config-statuses.md) for the provider-specific parameters and requirements.

