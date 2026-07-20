# Loopy Loyalty: Delete Location



```
DELETE https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/delete-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loopy Loyalty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/delete-location?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/delete-location?${params}`, {
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
| `id` | string | yes | Location ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignsAffected": [
        "string"
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignsAffected` | array<string> | Campaign IDs affected by the deletion. |
| `success` | boolean | Whether the location was deleted successfully. |

## Native endpoint

Through the native Loopy Loyalty API, this operation is `DELETE /location/:id` (base URL `https://api.loopyloyalty.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-location.md) for the provider-specific parameters and requirements.

