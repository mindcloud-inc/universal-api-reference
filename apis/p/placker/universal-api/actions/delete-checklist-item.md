# Placker: Delete Checklist Item



```
DELETE https://connect.mindcloud.co/v1/universal/placker/latest/actions/delete-checklist-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Placker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/placker/latest/actions/delete-checklist-item?connectionId=$CONNECTION_ID&checklist=sjwa8k5le5p1c&item=1234567890" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "checklist": "sjwa8k5le5p1c",
  "item": "1234567890"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/placker/latest/actions/delete-checklist-item?${params}`, {
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
| `checklist` | string | yes | Checklist ID. Example: `sjwa8k5le5p1c`. |
| `item` | string | yes | Checklist item ID. Example: `1234567890`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | Operation status. |

## Native endpoint

Through the native Placker API, this operation is `DELETE /checklist/:checklist/item/:item` (base URL `https://api.placker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-checklist-item.md) for the provider-specific parameters and requirements.

