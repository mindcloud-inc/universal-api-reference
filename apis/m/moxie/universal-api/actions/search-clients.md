# Moxie: Search Clients

Finds clients in Moxie.

```
GET https://connect.mindcloud.co/v1/universal/moxie/latest/actions/search-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moxie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moxie/latest/actions/search-clients?connectionId=$CONNECTION_ID&query=Moxie" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "Moxie"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moxie/latest/actions/search-clients?${params}`, {
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
| `query` | string | yes | Search text for matching clients. Example: `Moxie`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "address1": "string",
      "archive": true,
      "city": "string",
      "clientType": "string",
      "color": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "hourlyAmount": 1,
      "id": "string",
      "leadGenArchived": true,
      "locality": "string",
      "name": "Ava Chen",
      "paymentTerms": {
        "depositAmount": 1,
        "depositType": "string",
        "latePaymentFee": 1,
        "paymentDays": 1,
        "whoPaysCardFees": "string"
      },
      "peppolCompliant": true,
      "phone": "string",
      "postal": "string",
      "roundingIncrement": 1,
      "sampleData": true,
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `address1` | string |  |
| `archive` | boolean |  |
| `city` | string |  |
| `clientType` | string |  |
| `color` | string |  |
| `created` | date |  |
| `hourlyAmount` | number |  |
| `id` | string |  |
| `leadGenArchived` | boolean |  |
| `locality` | string |  |
| `name` | string |  |
| `paymentTerms.depositAmount` | number |  |
| `paymentTerms.depositType` | string |  |
| `paymentTerms.latePaymentFee` | number |  |
| `paymentTerms.paymentDays` | number |  |
| `paymentTerms.whoPaysCardFees` | string |  |
| `peppolCompliant` | boolean |  |
| `phone` | string |  |
| `postal` | string |  |
| `roundingIncrement` | number |  |
| `sampleData` | boolean |  |
| `website` | string |  |

## Native endpoint

Through the native Moxie API, this operation is `GET /action/clients/search` (base URL `https://pod01.withmoxie.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-clients.md) for the provider-specific parameters and requirements.

