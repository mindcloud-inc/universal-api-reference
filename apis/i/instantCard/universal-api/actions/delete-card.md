# InstantCard: Delete Card

Deletes an existing card from InstantCard.

```
DELETE https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/delete-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InstantCard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/delete-card?connectionId=$CONNECTION_ID&organizationId=20003827&id=3145927" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "20003827",
  "id": "3145927"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/delete-card?${params}`, {
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
| `organizationId` | number | yes | Organization ID from your InstantCard account. Example: `20003827`. |
| `id` | number | yes | ID of the card to delete. Example: `3145927`. |

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
| `result` | string |  |

## Native endpoint

Through the native InstantCard API, this operation is `DELETE /api/v2/organizations/:organizationId/cards/:id` (base URL `https://core.instantcard.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-card.md) for the provider-specific parameters and requirements.

