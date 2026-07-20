# Zillow MLS Data: List properties (OData)

Retrieves property records from Zillow MLS Data using OData.

```
GET https://connect.mindcloud.co/v1/universal/zillowMLSData/latest/actions/list-properties-o-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zillow MLS Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zillowMLSData/latest/actions/list-properties-o-data?connectionId=$CONNECTION_ID&dataset=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dataset": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zillowMLSData/latest/actions/list-properties-o-data?${params}`, {
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
| `dataset` | string | yes | Bridge dataset code that scopes the OData properties query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "BathroomsTotalDecimal": 1,
      "BathroomsTotalInteger": 1,
      "BedroomsTotal": 1,
      "City": "string",
      "ListAgentFullName": "Ava Chen",
      "ListingKey": "string",
      "ListOfficeName": "Ava Chen",
      "ListPrice": 1,
      "LivingArea": 1,
      "MlsStatus": "string",
      "ModificationTimestamp": "2026-05-07T12:00:00.000Z",
      "OriginatingSystemName": "Ava Chen",
      "PostalCode": "string",
      "PropertyType": "string",
      "StandardStatus": "string",
      "StateOrProvince": "string",
      "UnparsedAddress": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `BathroomsTotalDecimal` | number | Decimal bathroom count. |
| `BathroomsTotalInteger` | number | Integer bathroom count. |
| `BedroomsTotal` | number | Total bedrooms. |
| `City` | string | Listing city. |
| `ListAgentFullName` | string | Listing agent full name. |
| `ListingKey` | string | Primary listing key. |
| `ListOfficeName` | string | Listing office name. |
| `ListPrice` | number | Current list price. |
| `LivingArea` | number | Living area. |
| `MlsStatus` | string | MLS status. |
| `ModificationTimestamp` | date | Last listing modification timestamp. |
| `OriginatingSystemName` | string | Originating system name. |
| `PostalCode` | string | Listing postal code. |
| `PropertyType` | string | Property type. |
| `StandardStatus` | string | Standardized listing status. |
| `StateOrProvince` | string | Listing state or province. |
| `UnparsedAddress` | string | Full unparsed street address. |

## Native endpoint

Through the native Zillow MLS Data API, this operation is `GET /OData/:dataset/Properties` (base URL `https://api.bridgedataoutput.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-properties-o-data.md) for the provider-specific parameters and requirements.

