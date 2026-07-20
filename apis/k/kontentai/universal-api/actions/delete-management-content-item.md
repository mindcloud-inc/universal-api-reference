# Kontent.ai: Delete management content item

Deletes a content item from Kontent.ai.

```
DELETE https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/delete-management-content-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kontent.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/delete-management-content-item?connectionId=$CONNECTION_ID&itemIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "itemIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/delete-management-content-item?${params}`, {
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
| `itemIdentifier` | string | yes | Kontent.ai content item identifier to delete. |

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
| `success` | boolean | Whether the delete request completed successfully. |

## Native endpoint

Through the native Kontent.ai API, this operation is `DELETE https://manage.kontent.ai/v2/projects/:environment_id/items/:item_identifier` (base URL `https://deliver.kontent.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-management-content-item.md) for the provider-specific parameters and requirements.

