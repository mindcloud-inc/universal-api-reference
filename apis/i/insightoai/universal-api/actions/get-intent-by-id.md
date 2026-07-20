# Insighto.ai: Get Intent By Id



```
GET https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/get-intent-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insighto.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/get-intent-by-id?connectionId=$CONNECTION_ID&intentId=3c90c3cc-0d44-4b50-8888-8dd25736052a" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "intentId": "3c90c3cc-0d44-4b50-8888-8dd25736052a"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/get-intent-by-id?${params}`, {
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
| `intentId` | string | yes | The UUID id of the intent. Example: `3c90c3cc-0d44-4b50-8888-8dd25736052a`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "description": "string",
      "id": "string",
      "intent_type": "string",
      "is_active": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object |  |
| `description` | string |  |
| `id` | string |  |
| `intent_type` | string |  |
| `is_active` | boolean |  |
| `name` | string |  |

## Native endpoint

Through the native Insighto.ai API, this operation is `GET /intent/:intent_id` (base URL `https://api.insighto.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-intent-by-id.md) for the provider-specific parameters and requirements.

