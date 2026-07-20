# Easy-Peasy.AI: List Presets

Retrieves text generation presets from Easy-Peasy.AI.

```
GET https://connect.mindcloud.co/v1/universal/easyPeasyAI/latest/actions/list-presets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easy-Peasy.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyPeasyAI/latest/actions/list-presets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyPeasyAI/latest/actions/list-presets?${params}`, {
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
| `category` | string | no | Optional preset category filter documented by Easy-Peasy.AI. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Easy-Peasy.AI API returns.

## Native endpoint

Through the native Easy-Peasy.AI API, this operation is `GET /api/presets` (base URL `https://easy-peasy.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-presets.md) for the provider-specific parameters and requirements.

