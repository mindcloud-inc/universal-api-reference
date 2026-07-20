# Atera: Get customer

Retrieves a customer from Atera by ID.

```
GET https://connect.mindcloud.co/v1/universal/atera/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atera `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atera/latest/actions/get-customer?connectionId=$CONNECTION_ID&customerId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atera/latest/actions/get-customer?${params}`, {
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
| `customerId` | number | yes | System customer ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Country": "string",
      "CreatedOn": "string",
      "CustomerID": 1,
      "CustomerName": "Ava Chen",
      "LastModified": "string",
      "Latitude": 1,
      "Longitude": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Country` | string |  |
| `CreatedOn` | string |  |
| `CustomerID` | number |  |
| `CustomerName` | string |  |
| `LastModified` | string |  |
| `Latitude` | number |  |
| `Longitude` | number |  |

## Native endpoint

Through the native Atera API, this operation is `GET /api/v3/customers/:customerId` (base URL `https://app.atera.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

