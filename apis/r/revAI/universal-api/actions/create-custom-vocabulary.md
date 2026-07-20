# Rev AI: Create Custom Vocabulary

Creates a custom vocabulary in Rev AI.

```
POST https://connect.mindcloud.co/v1/universal/revAI/latest/actions/create-custom-vocabulary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rev AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/revAI/latest/actions/create-custom-vocabulary" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customVocabularies[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/revAI/latest/actions/create-custom-vocabulary', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customVocabularies[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customVocabularies[]` | array<object> | yes |  |
| `metadata` | string | no |  |
| `strict` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callbackUrl": "https://example.com",
      "completedOn": "string",
      "createdOn": "string",
      "failure": "string",
      "failureDetail": "string",
      "id": "string",
      "metadata": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callbackUrl` | string |  |
| `completedOn` | string |  |
| `createdOn` | string |  |
| `failure` | string |  |
| `failureDetail` | string |  |
| `id` | string |  |
| `metadata` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Rev AI API, this operation is `POST /speechtotext/v1/vocabularies` (base URL `https://api.rev.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-custom-vocabulary.md) for the provider-specific parameters and requirements.

