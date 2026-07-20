# Datarobot: List Custom Model Versions

Retrieves versions for a custom model from Datarobot.

```
GET https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/list-custom-model-versions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datarobot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/list-custom-model-versions?connectionId=$CONNECTION_ID&customModelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customModelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/list-custom-model-versions?${params}`, {
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
| `customModelId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "customModelId": "string",
      "description": "string",
      "id": "string",
      "label": "string",
      "versionMajor": 1,
      "versionMinor": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `customModelId` | string |  |
| `description` | string |  |
| `id` | string |  |
| `label` | string |  |
| `versionMajor` | number |  |
| `versionMinor` | number |  |

## Native endpoint

Through the native Datarobot API, this operation is `GET /customModels/:customModelId/versions/` (base URL `https://app.datarobot.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-custom-model-versions.md) for the provider-specific parameters and requirements.

