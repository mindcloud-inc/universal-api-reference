# Edoobox: Delete Offer

Deletes an existing offer from Edoobox.

```
DELETE https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/delete-offer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edoobox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/delete-offer?connectionId=$CONNECTION_ID&offerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "offerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/delete-offer?${params}`, {
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
| `offerId` | string | yes | edoobox offer ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "delete": true,
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `delete` | boolean |  |
| `id` | string |  |

## Native endpoint

Through the native Edoobox API, this operation is `DELETE /offer/:offer_id` (base URL `https://app2.edoobox.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-offer.md) for the provider-specific parameters and requirements.

