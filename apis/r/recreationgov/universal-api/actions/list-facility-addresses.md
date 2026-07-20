# Recreation.gov: List Facility Addresses

Retrieves addresses for a facility from Recreation.gov.

```
GET https://connect.mindcloud.co/v1/universal/recreationgov/latest/actions/list-facility-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recreation.gov `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recreationgov/latest/actions/list-facility-addresses?connectionId=$CONNECTION_ID&limit=25&offset=0&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recreationgov/latest/actions/list-facility-addresses?${params}`, {
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
| `id` | number | yes |  |
| `query` | string | no | Filter addresses by city, state, postal code, country code, or street fields. |
| `limit` | number | no | Maximum number of records to return. |
| `offset` | number | no | Number of records to skip before returning results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AddressCountryCode": "string",
      "AddressStateCode": "string",
      "City": "string",
      "FacilityAddressID": "string",
      "FacilityAddressType": "string",
      "FacilityID": "string",
      "FacilityStreetAddress1": "string",
      "FacilityStreetAddress2": "string",
      "FacilityStreetAddress3": "string",
      "LastUpdatedDate": "string",
      "PostalCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AddressCountryCode` | string |  |
| `AddressStateCode` | string |  |
| `City` | string |  |
| `FacilityAddressID` | string |  |
| `FacilityAddressType` | string |  |
| `FacilityID` | string |  |
| `FacilityStreetAddress1` | string |  |
| `FacilityStreetAddress2` | string |  |
| `FacilityStreetAddress3` | string |  |
| `LastUpdatedDate` | string |  |
| `PostalCode` | string |  |

## Native endpoint

Through the native Recreation.gov API, this operation is `GET /facilities/{id}/facilityaddresses` (base URL `https://ridb.recreation.gov/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-facility-addresses.md) for the provider-specific parameters and requirements.

