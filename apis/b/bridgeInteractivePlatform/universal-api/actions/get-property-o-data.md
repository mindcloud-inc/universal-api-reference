# Bridge Interactive Platform: Get property (OData)

Retrieves a property from Bridge Interactive Platform.

```
GET https://connect.mindcloud.co/v1/universal/bridgeInteractivePlatform/latest/actions/get-property-o-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridge Interactive Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridgeInteractivePlatform/latest/actions/get-property-o-data?connectionId=$CONNECTION_ID&dataset=test&ListingKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dataset": "test",
  "ListingKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridgeInteractivePlatform/latest/actions/get-property-o-data?${params}`, {
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
| `dataset` | string | yes | Bridge dataset code. This tenant was validated against dataset test. Default: `test`. |
| `ListingKey` | string | yes | OData property identifier from Bridge. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "City": "string",
      "ListingId": "string",
      "ListingKey": "string",
      "ListPrice": 1,
      "MlsStatus": "string",
      "PropertyType": "string",
      "StateOrProvince": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `City` | string |  |
| `ListingId` | string |  |
| `ListingKey` | string |  |
| `ListPrice` | number |  |
| `MlsStatus` | string |  |
| `PropertyType` | string |  |
| `StateOrProvince` | string |  |

## Native endpoint

Through the native Bridge Interactive Platform API, this operation is `GET /OData/:dataset/Property(':ListingKey')` (base URL `https://api.bridgedataoutput.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-property-o-data.md) for the provider-specific parameters and requirements.

