# CAMB.AI: Fetch Bulk Translation Results

Retrieves multiple translation results from CAMB.AI.

```
GET https://connect.mindcloud.co/v1/universal/cAMBAI/latest/actions/fetch-bulk-translation-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CAMB.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cAMBAI/latest/actions/fetch-bulk-translation-results?connectionId=$CONNECTION_ID&runIds%5B%5D=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "runIds[]": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cAMBAI/latest/actions/fetch-bulk-translation-results?${params}`, {
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
| `runIds[]` | array<number> | yes | Two to five completed translation run identifiers. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CAMB.AI API returns.

## Native endpoint

Through the native CAMB.AI API, this operation is `POST /translation-results` (base URL `https://client.camb.ai/apis`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-bulk-translation-results.md) for the provider-specific parameters and requirements.

