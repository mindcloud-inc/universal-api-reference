# Coast: Get Card By ID



```
GET https://connect.mindcloud.co/v1/universal/coast/latest/actions/getcard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coast/latest/actions/getcard?connectionId=$CONNECTION_ID&cardId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cardId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coast/latest/actions/getcard?${params}`, {
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
| `cardId` | string | yes | Coast card ID of the card to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "assignedPersonId": {},
      "fleetCardId": "string",
      "gasStationRestriction": "string",
      "id": "string",
      "last4": "string",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `assignedPersonId` | object |  |
| `fleetCardId` | string |  |
| `gasStationRestriction` | string |  |
| `id` | string |  |
| `last4` | string |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Coast API, this operation is `GET /v2/cards/:cardId` (base URL `https://public.coastpay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/getcard.md) for the provider-specific parameters and requirements.

