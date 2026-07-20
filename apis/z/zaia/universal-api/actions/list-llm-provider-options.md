# Zaia: List LLM Provider Options

Retrieves LLM provider options from your Zaia workspace.

```
GET https://connect.mindcloud.co/v1/universal/zaia/latest/actions/list-llm-provider-options
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zaia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zaia/latest/actions/list-llm-provider-options?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zaia/latest/actions/list-llm-provider-options?${params}`, {
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
      "aiLab": "string",
      "artificialAnalysisReference": "string",
      "cost": 1,
      "indicators": {},
      "label": "string",
      "name": "Ava Chen",
      "provider": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aiLab` | string | AI lab or model family owner. |
| `artificialAnalysisReference` | string | Artificial Analysis model reference key. |
| `cost` | number | Relative model cost value. |
| `indicators` | object | Provider model indicator flags and score. |
| `label` | string | Human-readable model label. |
| `name` | string | Model key. |
| `provider` | string | Provider key. |

## Native endpoint

Through the native Zaia API, this operation is `GET /api/v1/llm-providers/options` (base URL `https://api.endless.zaia.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-llm-provider-options.md) for the provider-specific parameters and requirements.

