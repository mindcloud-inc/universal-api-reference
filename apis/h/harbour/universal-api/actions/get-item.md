# Harbour: Get Item

Retrieves a specific item from Harbour.

```
GET https://connect.mindcloud.co/v1/universal/harbour/latest/actions/get-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harbour `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harbour/latest/actions/get-item?connectionId=$CONNECTION_ID&item_id=Pr6GqXoA" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "item_id": "Pr6GqXoA"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harbour/latest/actions/get-item?${params}`, {
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
| `item_id` | string | yes | Unique Harbour item identifier. Example: `Pr6GqXoA`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "item": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `item` | object |  |

## Native endpoint

Through the native Harbour API, this operation is `GET https://api.harbourshare.com/v1/items/:item_id` (base URL `https://api.myharbourshare.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-item.md) for the provider-specific parameters and requirements.

