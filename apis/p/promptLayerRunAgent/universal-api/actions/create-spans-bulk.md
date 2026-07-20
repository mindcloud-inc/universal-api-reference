# PromptLayer Run Agent: Create Spans Bulk

Creates spans in bulk in PromptLayer.

```
POST https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/create-spans-bulk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PromptLayer Run Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/create-spans-bulk" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "spans[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/create-spans-bulk', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "spans[]": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `spans[]` | array<object> | yes | Array of span objects to create in PromptLayer. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "spans": [
        {}
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `spans` | array<object> | Created span records returned by PromptLayer. |
| `success` | boolean | Whether PromptLayer created the spans. |

## Native endpoint

Through the native PromptLayer Run Agent API, this operation is `POST /spans-bulk` (base URL `https://api.promptlayer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-spans-bulk.md) for the provider-specific parameters and requirements.

