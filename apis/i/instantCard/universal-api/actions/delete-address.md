# InstantCard: Delete Address

Deletes an existing address from InstantCard.

```
DELETE https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/delete-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InstantCard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/delete-address?connectionId=$CONNECTION_ID&id=1&organizationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1",
  "organizationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/delete-address?${params}`, {
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
| `id` | number | yes | Address ID from InstantCard. |
| `organizationId` | number | yes | Organization ID from InstantCard. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string | Deletion result. |

## Native endpoint

Through the native InstantCard API, this operation is `DELETE /api/v2/organizations/:organizationId/addresses/:id` (base URL `https://core.instantcard.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-address.md) for the provider-specific parameters and requirements.

