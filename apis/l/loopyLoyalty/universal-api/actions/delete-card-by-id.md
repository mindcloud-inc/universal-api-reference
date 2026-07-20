# Loopy Loyalty: Delete Card By ID



```
DELETE https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/delete-card-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loopy Loyalty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/delete-card-by-id?connectionId=$CONNECTION_ID&id=RDX5AsgKYa3UZ7" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "RDX5AsgKYa3UZ7"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/delete-card-by-id?${params}`, {
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
| `id` | string | yes | Example: `RDX5AsgKYa3UZ7`. |

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
| `success` | boolean | Whether the card was deleted successfully. |

## Native endpoint

Through the native Loopy Loyalty API, this operation is `DELETE /card/cid/:id/delete` (base URL `https://api.loopyloyalty.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-card-by-id.md) for the provider-specific parameters and requirements.

