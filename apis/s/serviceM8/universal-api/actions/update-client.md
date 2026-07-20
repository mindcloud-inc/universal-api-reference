# ServiceM8: Update Client



```
PUT https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/update-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceM8 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/update-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uuid": "550e8400-e29b-41d4-a716-446655440000"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/update-client', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uuid": "550e8400-e29b-41d4-a716-446655440000"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uuid` | string | yes | Example: `550e8400-e29b-41d4-a716-446655440000`. |
| `name` | string | no |  |
| `abnNumber` | string | no |  |
| `address` | string | no |  |
| `billingAddress` | string | no |  |
| `parentCompanyUuid` | string | no |  |
| `website` | string | no | Example: `https://example.com`. |
| `addressStreet` | string | no |  |
| `addressCity` | string | no |  |
| `addressState` | string | no |  |
| `addressPostcode` | string | no |  |
| `addressCountry` | string | no |  |
| `faxNumber` | string | no | Example: `+1 555 123 4567`. |
| `badges` | string | no |  |
| `taxRateUuid` | string | no |  |
| `billingAttention` | string | no |  |
| `paymentTerms` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "recordUuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `recordUuid` | string | UUID of the updated client. |

## Native endpoint

Through the native ServiceM8 API, this operation is `POST /api_1.0/company/:uuid.json` (base URL `https://api.servicem8.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-client.md) for the provider-specific parameters and requirements.

