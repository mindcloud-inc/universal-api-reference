# Escrow.com: Get Milestone Item Web URL

Retrieves a milestone item web URL from Escrow.com.

```
GET https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/get-milestone-item-web-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Escrow.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/get-milestone-item-web-url?connectionId=$CONNECTION_ID&transactionId=1&itemId=1&action=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transactionId": "1",
  "itemId": "1",
  "action": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/get-milestone-item-web-url?${params}`, {
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
| `transactionId` | number | yes | The Escrow.com transaction ID. |
| `itemId` | number | yes | The milestone item ID. |
| `action` | string | yes | Web action to perform on this milestone item. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `asCustomer` | string | no | Escrow.com customer email to send as the As-Customer header when acting as a partner on behalf of a party. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "landingPage": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `landingPage` | string | Escrow.com hosted page URL for the milestone item action. |

## Native endpoint

Through the native Escrow.com API, this operation is `GET /transaction/:transaction_id/item/:item_id/web_link/:action` (base URL `https://api.escrow-sandbox.com/2017-09-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-milestone-item-web-url.md) for the provider-specific parameters and requirements.

