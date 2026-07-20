# Quickbase: Delete Field(s)

Deletes existing fields from a Quickbase table.

```
DELETE https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/delete-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quickbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/delete-fields?connectionId=$CONNECTION_ID&tableId=string&fieldIds%5B%5D=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tableId": "string",
  "fieldIds[]": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/delete-fields?${params}`, {
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
| `tableId` | string | yes | The Quickbase table that contains the fields to delete. |
| `fieldIds[]` | array<number> | yes | The list of Quickbase field IDs to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deletedFieldIds": [
        1
      ],
      "errors": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deletedFieldIds` | array<number> | The Quickbase field IDs that were deleted. |
| `errors` | array<string> | Any field deletion errors returned by Quickbase. |

## Native endpoint

Through the native Quickbase API, this operation is `DELETE v1/fields` (base URL `https://api.quickbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-fields.md) for the provider-specific parameters and requirements.

