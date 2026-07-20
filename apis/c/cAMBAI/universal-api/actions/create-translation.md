# CAMB.AI: Create Translation

Creates a new translation task in CAMB.AI.

```
POST https://connect.mindcloud.co/v1/universal/cAMBAI/latest/actions/create-translation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CAMB.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cAMBAI/latest/actions/create-translation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sourceLanguageId": 1,
  "targetLanguageId": 1,
  "texts[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cAMBAI/latest/actions/create-translation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sourceLanguageId": 1,
    "targetLanguageId": 1,
    "texts[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceLanguageId` | number | yes | Source language identifier from Get Source Languages. |
| `targetLanguageId` | number | yes | Target language identifier from Get Target Languages. |
| `texts[]` | array<string> | yes | One or more text segments to translate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "run_id": 1,
      "task_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `run_id` | number | Run identifier when immediately available in the create response. |
| `task_id` | string | Task identifier for the translation request. |

## Native endpoint

Through the native CAMB.AI API, this operation is `POST /translate` (base URL `https://client.camb.ai/apis`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-translation.md) for the provider-specific parameters and requirements.

