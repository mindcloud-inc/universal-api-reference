# Rev AI: Get Custom Vocabulary

Retrieves a custom vocabulary from Rev AI.

```
GET https://connect.mindcloud.co/v1/universal/revAI/latest/actions/get-custom-vocabulary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rev AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/revAI/latest/actions/get-custom-vocabulary?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/revAI/latest/actions/get-custom-vocabulary?${params}`, {
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
| `id` | string | yes |  |

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

Through the native Rev AI API, this operation is `GET /speechtotext/v1/vocabularies/:id` (base URL `https://api.rev.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-custom-vocabulary.md) for the provider-specific parameters and requirements.

