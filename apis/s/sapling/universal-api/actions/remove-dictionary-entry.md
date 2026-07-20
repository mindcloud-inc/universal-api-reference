# Sapling: Remove Dictionary Entry

Deletes a dictionary entry from Sapling.

```
DELETE https://connect.mindcloud.co/v1/universal/sapling/latest/actions/remove-dictionary-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sapling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sapling/latest/actions/remove-dictionary-entry?connectionId=$CONNECTION_ID&dictionaryEntryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dictionaryEntryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sapling/latest/actions/remove-dictionary-entry?${params}`, {
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
| `dictionaryEntryId` | string | yes | UUID of the dictionary entry to remove. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sapling API returns.

## Native endpoint

Through the native Sapling API, this operation is `DELETE /api/v1/dictionary/:dictionaryEntryId` (base URL `https://api.sapling.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-dictionary-entry.md) for the provider-specific parameters and requirements.

