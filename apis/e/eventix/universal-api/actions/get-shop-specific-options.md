# Eventix: Get a specific Shop's options

Retrieves options for an Eventix shop.

```
GET https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-shop-specific-options
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-shop-specific-options?connectionId=$CONNECTION_ID&guid=shop-guid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "guid": "shop-guid"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-shop-specific-options?${params}`, {
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
| `guid` | string | yes | The guid of the Shop. Example: `shop-guid`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allow_order_return": true,
      "allow_user_return": true,
      "arbitrary": true,
      "callback": true,
      "insert": true,
      "late_personalization": true,
      "payment": true,
      "pdf": true,
      "receipt": true,
      "report": true,
      "reservations": true,
      "return": true,
      "send_email": true,
      "skip_metadata_validation": true,
      "to_zero": true,
      "validate": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allow_order_return` | boolean |  |
| `allow_user_return` | boolean |  |
| `arbitrary` | boolean |  |
| `callback` | boolean |  |
| `insert` | boolean |  |
| `late_personalization` | boolean |  |
| `payment` | boolean |  |
| `pdf` | boolean |  |
| `receipt` | boolean |  |
| `report` | boolean |  |
| `reservations` | boolean |  |
| `return` | boolean |  |
| `send_email` | boolean |  |
| `skip_metadata_validation` | boolean |  |
| `to_zero` | boolean |  |
| `validate` | boolean |  |

## Native endpoint

Through the native Eventix API, this operation is `GET /3.0.0/shop/:guid/options` (base URL `https://api.weeztix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shop-specific-options.md) for the provider-specific parameters and requirements.

