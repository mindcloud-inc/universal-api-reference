# AITable.ai: Delete Records

Deletes existing records from a datasheet in AITable.ai.

```
DELETE https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/delete-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AITable.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/delete-records?connectionId=$CONNECTION_ID&datasheetId=string&recordIds=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "datasheetId": "string",
  "recordIds": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/delete-records?${params}`, {
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
| `datasheetId` | string | yes | AITable datasheet ID containing records to delete. |
| `recordIds` | string<string> | yes | One or more AITable record IDs to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AITable.ai API returns.

## Native endpoint

Through the native AITable.ai API, this operation is `DELETE /fusion/v1/datasheets/:datasheetId/records` (base URL `https://aitable.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-records.md) for the provider-specific parameters and requirements.

