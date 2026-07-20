# Recreation.gov: Update Facility Address

Updates a facility address in Recreation.gov.

```
PUT https://connect.mindcloud.co/v1/universal/recreationgov/latest/actions/update-facility-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recreation.gov `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/recreationgov/latest/actions/update-facility-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "addressId": 1,
  "stateCode": "string",
  "countryCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recreationgov/latest/actions/update-facility-address', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "addressId": 1,
    "stateCode": "string",
    "countryCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes |  |
| `type` | string | no |  |
| `address1` | string | no |  |
| `addressId` | number | yes |  |
| `address2` | string | no |  |
| `address3` | string | no |  |
| `city` | string | no |  |
| `postalCode` | string | no |  |
| `stateCode` | string | yes |  |
| `countryCode` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "MESSAGE": "string",
      "STATUSCODE": 1,
      "SUCCESS": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `MESSAGE` | string |  |
| `STATUSCODE` | number |  |
| `SUCCESS` | boolean |  |

## Native endpoint

Through the native Recreation.gov API, this operation is `PUT /facilities/{id}/facilityaddresses/{addressId}` (base URL `https://ridb.recreation.gov/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-facility-address.md) for the provider-specific parameters and requirements.

