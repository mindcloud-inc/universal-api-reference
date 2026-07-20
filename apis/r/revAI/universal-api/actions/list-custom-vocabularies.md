# Rev AI: List Custom Vocabularies

Retrieves custom vocabularies from Rev AI.

```
GET https://connect.mindcloud.co/v1/universal/revAI/latest/actions/list-custom-vocabularies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rev AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/revAI/latest/actions/list-custom-vocabularies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/revAI/latest/actions/list-custom-vocabularies?${params}`, {
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

Through the native Rev AI API, this operation is `GET /speechtotext/v1/vocabularies` (base URL `https://api.rev.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-custom-vocabularies.md) for the provider-specific parameters and requirements.

