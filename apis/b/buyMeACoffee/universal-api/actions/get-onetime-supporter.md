# Buy Me a Coffee: Get Onetime Supporter

Retrieves one-time supporter details from Buy Me a Coffee by supporter ID.

```
GET https://connect.mindcloud.co/v1/universal/buyMeACoffee/latest/actions/get-onetime-supporter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Buy Me a Coffee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buyMeACoffee/latest/actions/get-onetime-supporter?connectionId=$CONNECTION_ID&id=76789" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "76789"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buyMeACoffee/latest/actions/get-onetime-supporter?${params}`, {
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
| `id` | number | yes | The unique ID of the supporter returned by the list supporters action. Example: `76789`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "isRefunded": true,
      "payerEmail": "ava@example.com",
      "payerName": "Ava Chen",
      "paymentPlatform": "string",
      "referer": "string",
      "supportCoffeePrice": "string",
      "supportCoffees": 1,
      "supportCreatedOn": "2026-05-07T12:00:00.000Z",
      "supportCurrency": "string",
      "supportEmail": "ava@example.com",
      "supporterName": "Ava Chen",
      "supportId": 1,
      "supportNote": "string",
      "supportNotePinned": 1,
      "supportUpdatedOn": "2026-05-07T12:00:00.000Z",
      "supportVisibility": 1,
      "transactionId": "string",
      "transferId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string |  |
| `isRefunded` | boolean |  |
| `payerEmail` | string |  |
| `payerName` | string |  |
| `paymentPlatform` | string |  |
| `referer` | string |  |
| `supportCoffeePrice` | string |  |
| `supportCoffees` | number |  |
| `supportCreatedOn` | date |  |
| `supportCurrency` | string |  |
| `supportEmail` | string |  |
| `supporterName` | string |  |
| `supportId` | number |  |
| `supportNote` | string |  |
| `supportNotePinned` | number |  |
| `supportUpdatedOn` | date |  |
| `supportVisibility` | number |  |
| `transactionId` | string |  |
| `transferId` | string |  |

## Native endpoint

Through the native Buy Me a Coffee API, this operation is `GET /supporters/:id` (base URL `https://developers.buymeacoffee.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-onetime-supporter.md) for the provider-specific parameters and requirements.

