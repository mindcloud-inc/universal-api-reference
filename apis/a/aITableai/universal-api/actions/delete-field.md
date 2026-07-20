# AITable.ai: Delete Field

Deletes an existing datasheet field from AITable.ai.

```
DELETE https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/delete-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AITable.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/delete-field?connectionId=$CONNECTION_ID&spaceId=string&datasheetId=string&fieldId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "spaceId": "string",
  "datasheetId": "string",
  "fieldId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/delete-field?${params}`, {
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
| `spaceId` | string | yes | AITable space ID containing the datasheet. |
| `datasheetId` | string | yes | AITable datasheet ID containing the field. |
| `fieldId` | string | yes | AITable field ID to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AITable.ai API returns.

## Native endpoint

Through the native AITable.ai API, this operation is `DELETE /fusion/v1/spaces/:spaceId/datasheets/:datasheetId/fields/:fieldId` (base URL `https://aitable.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-field.md) for the provider-specific parameters and requirements.

