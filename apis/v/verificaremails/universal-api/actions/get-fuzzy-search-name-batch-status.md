# Verificaremails: Get Fuzzy Search Name Batch Status

Retrieves a fuzzy search name batch validation status from Verificaremails.

```
GET https://connect.mindcloud.co/v1/universal/verificaremails/latest/actions/get-fuzzy-search-name-batch-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verificaremails `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verificaremails/latest/actions/get-fuzzy-search-name-batch-status?connectionId=$CONNECTION_ID&requestId=Provider%20request%20ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestId": "Provider request ID"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/verificaremails/latest/actions/get-fuzzy-search-name-batch-status?${params}`, {
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
| `requestId` | string | yes | Batch request ID returned when the fuzzy search name batch validation was created. Example: `Provider request ID`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Verificaremails API returns.

## Native endpoint

Through the native Verificaremails API, this operation is `GET /fuzzysearch/status/{{requestId}}` (base URL `https://dashboard.verificaremails.com/myapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-fuzzy-search-name-batch-status.md) for the provider-specific parameters and requirements.

