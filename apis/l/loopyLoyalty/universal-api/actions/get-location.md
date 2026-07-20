# Loopy Loyalty: Get Location



```
GET https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/get-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loopy Loyalty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/get-location?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/get-location?${params}`, {
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
      "address": "string",
      "id": "string",
      "lat": 1,
      "lon": 1,
      "name": "Ava Chen",
      "object": "string",
      "showAddressOnCard": true,
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string | Human readable address. |
| `id` | string | Location ID. |
| `lat` | number | Latitude. |
| `lon` | number | Longitude. |
| `name` | string | Location name. |
| `object` | string | Resource type marker. |
| `showAddressOnCard` | boolean | Whether the address is shown on the card. |
| `uid` | string | Owner user ID. |

## Native endpoint

Through the native Loopy Loyalty API, this operation is `GET /location/:id` (base URL `https://api.loopyloyalty.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-location.md) for the provider-specific parameters and requirements.

