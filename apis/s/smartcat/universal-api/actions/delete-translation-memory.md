# Smartcat: Delete Translation Memory

Deletes a translation memory from Smartcat.

```
DELETE https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/delete-translation-memory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smartcat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/delete-translation-memory?connectionId=$CONNECTION_ID&tmId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tmId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/delete-translation-memory?${params}`, {
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
| `tmId` | string | yes | Smartcat translation memory ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Smartcat API returns.

## Native endpoint

Through the native Smartcat API, this operation is `DELETE /api/integration/v1/translationmemory/:tmId` (base URL `https://smartcat.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-translation-memory.md) for the provider-specific parameters and requirements.

