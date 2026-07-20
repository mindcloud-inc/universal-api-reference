# ServiceM8: Get Client



```
GET https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/get-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceM8 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/get-client?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/get-client?${params}`, {
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
| `uuid` | string | yes | Record UUID of the client to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "abnNumber": "string",
      "active": 1,
      "address": "string",
      "addressCity": "string",
      "addressCountry": "string",
      "addressPostcode": "string",
      "addressState": "string",
      "addressStreet": "string",
      "badges": "string",
      "billingAddress": "string",
      "billingAttention": "string",
      "editDate": "2026-05-07T12:00:00.000Z",
      "faxNumber": "string",
      "isIndividual": 1,
      "name": "Ava Chen",
      "paymentTerms": "string",
      "taxRateUuid": "string",
      "uuid": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `abnNumber` | string |  |
| `active` | number |  |
| `address` | string |  |
| `addressCity` | string |  |
| `addressCountry` | string |  |
| `addressPostcode` | string |  |
| `addressState` | string |  |
| `addressStreet` | string |  |
| `badges` | string |  |
| `billingAddress` | string |  |
| `billingAttention` | string |  |
| `editDate` | date |  |
| `faxNumber` | string |  |
| `isIndividual` | number |  |
| `name` | string |  |
| `paymentTerms` | string |  |
| `taxRateUuid` | string |  |
| `uuid` | string |  |
| `website` | string |  |

## Native endpoint

Through the native ServiceM8 API, this operation is `GET /api_1.0/company/:uuid.json` (base URL `https://api.servicem8.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client.md) for the provider-specific parameters and requirements.

