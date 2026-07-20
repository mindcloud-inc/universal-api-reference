# PostcardMania: Remove Suppressed Address

Deletes an existing suppressed address from PostcardMania.

```
DELETE https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/remove-suppressed-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostcardMania `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/remove-suppressed-address?connectionId=$CONNECTION_ID&suppressionAddressID=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "suppressionAddressID": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/remove-suppressed-address?${params}`, {
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
| `suppressionAddressID` | number | yes | Suppression list entry identifier. |

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
| `success` | boolean | Whether the suppressed address was removed successfully. |

## Native endpoint

Through the native PostcardMania API, this operation is `DELETE /suppression-list/{{suppressionAddressID}}` (base URL `https://v3.pcmintegrations.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-suppressed-address.md) for the provider-specific parameters and requirements.

