# Blaze AI: Get Published Docs Polling Test

Retrieves published document polling test data from Blaze AI.

```
GET https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/get-published-docs-polling-test
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blaze AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/get-published-docs-polling-test?connectionId=$CONNECTION_ID&workspace_id=994619" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspace_id": "994619"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/get-published-docs-polling-test?${params}`, {
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
| `workspace_id` | number | yes | Default: `994619`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Blaze AI API, this operation is `GET /api/v1/w/:workspace_id/zapier_published_docs_polling_test` (base URL `https://api.blaze.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-published-docs-polling-test.md) for the provider-specific parameters and requirements.

