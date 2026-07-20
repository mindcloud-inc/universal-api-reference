# Uwear.ai: Delete Clothing Item

Deletes an existing clothing item from Uwear.ai.

```
DELETE https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/delete-clothing-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uwear.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/delete-clothing-item?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/delete-clothing-item?${params}`, {
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
| `clothing_item_id` | string | no | The clothing item ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "detail": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `detail` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Uwear.ai API, this operation is `DELETE /api/v1/clothing-item/:clothing_item_id` (base URL `https://api.uwear.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-clothing-item.md) for the provider-specific parameters and requirements.

