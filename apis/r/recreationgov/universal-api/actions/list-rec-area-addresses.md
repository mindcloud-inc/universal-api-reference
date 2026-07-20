# Recreation.gov: List Rec Area Addresses

Retrieves addresses for a recreation area from Recreation.gov.

```
GET https://connect.mindcloud.co/v1/universal/recreationgov/latest/actions/list-rec-area-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recreation.gov `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recreationgov/latest/actions/list-rec-area-addresses?connectionId=$CONNECTION_ID&limit=25&offset=0&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recreationgov/latest/actions/list-rec-area-addresses?${params}`, {
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
      "LastUpdatedDate": "string",
      "PostalCode": "string",
      "RecAreaAddressID": "string",
      "RecAreaAddressType": "string",
      "RecAreaID": "string",
      "RecAreaStreetAddress1": "string",
      "RecAreaStreetAddress2": "string",
      "RecAreaStreetAddress3": "string"
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
| `LastUpdatedDate` | string |  |
| `PostalCode` | string |  |
| `RecAreaAddressID` | string |  |
| `RecAreaAddressType` | string |  |
| `RecAreaID` | string |  |
| `RecAreaStreetAddress1` | string |  |
| `RecAreaStreetAddress2` | string |  |
| `RecAreaStreetAddress3` | string |  |

## Native endpoint

Through the native Recreation.gov API, this operation is `GET /recareas/{id}/recareaaddresses` (base URL `https://ridb.recreation.gov/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-rec-area-addresses.md) for the provider-specific parameters and requirements.

