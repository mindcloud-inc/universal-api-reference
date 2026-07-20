# Raklet: Add Contact Address



```
POST https://connect.mindcloud.co/v1/universal/raklet/latest/actions/add-contact-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raklet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/raklet/latest/actions/add-contact-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organisationMembershipId": "string",
  "details": "string",
  "city": "string",
  "country": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/raklet/latest/actions/add-contact-address', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organisationMembershipId": "string",
    "details": "string",
    "city": "string",
    "country": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organisationMembershipId` | string | yes | Raklet contact membership identifier for the address owner. |
| `details` | string | yes | Street or line details for the address. |
| `city` | string | yes | City for the address. |
| `country` | string | yes | Country code or country value expected by Raklet for the address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {
        "city": "string",
        "country": "string",
        "county": "string",
        "details": "string",
        "fullAddress": "string",
        "id": "string",
        "postalCode": "string",
        "state": "string"
      },
      "errors": [
        {}
      ],
      "isSuccess": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | Raklet response code. |
| `data.city` | string | Address city. |
| `data.country` | string | Address country. |
| `data.county` | string | County value returned by Raklet. |
| `data.details` | string | Address line details. |
| `data.fullAddress` | string | Combined full address string. |
| `data.id` | string | Raklet address identifier. |
| `data.postalCode` | string | Postal code returned by Raklet. |
| `data.state` | string | Address state. |
| `errors` | array<object> | Raklet error collection. |
| `isSuccess` | boolean | Whether Raklet marked the request successful. |

## Native endpoint

Through the native Raklet API, this operation is `POST /organisations/:organisationId/contacts/:organisationMembershipId/addresses` (base URL `https://api.raklet.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-contact-address.md) for the provider-specific parameters and requirements.

