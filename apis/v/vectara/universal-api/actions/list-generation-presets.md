# Vectara: List Generation Presets

Retrieves available generation presets from Vectara.

```
GET https://connect.mindcloud.co/v1/universal/vectara/latest/actions/list-generation-presets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vectara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vectara/latest/actions/list-generation-presets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vectara/latest/actions/list-generation-presets?${params}`, {
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
| `llmName` | string | no | Filter generation presets by LLM name. |
| `limit` | number | no | Maximum number of presets to return. |
| `pageKey` | string | no | Cursor for the next page of generation presets. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "generation_presets": [
        {}
      ],
      "metadata": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `generation_presets` | array<object> | List of generation presets. |
| `metadata` | object | Pagination metadata for the list response. |

## Native endpoint

Through the native Vectara API, this operation is `GET /v2/generation_presets` (base URL `https://api.vectara.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-generation-presets.md) for the provider-specific parameters and requirements.

