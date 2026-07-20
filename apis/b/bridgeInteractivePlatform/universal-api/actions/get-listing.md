# Bridge Interactive Platform: Get listing

Retrieves a listing from Bridge Interactive Platform.

```
GET https://connect.mindcloud.co/v1/universal/bridgeInteractivePlatform/latest/actions/get-listing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridge Interactive Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridgeInteractivePlatform/latest/actions/get-listing?connectionId=$CONNECTION_ID&dataset=test&listingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dataset": "test",
  "listingId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridgeInteractivePlatform/latest/actions/get-listing?${params}`, {
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
| `listingId` | string | yes | Bridge listing identifier from the REST listings feed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ListingId": "string",
      "ListingKey": "string",
      "ListPrice": 1,
      "MlsStatus": "string",
      "ModificationTimestamp": "2026-05-07T12:00:00.000Z",
      "PropertyType": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ListingId` | string |  |
| `ListingKey` | string |  |
| `ListPrice` | number |  |
| `MlsStatus` | string |  |
| `ModificationTimestamp` | date |  |
| `PropertyType` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Bridge Interactive Platform API, this operation is `GET /:dataset/listings/:listingId` (base URL `https://api.bridgedataoutput.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-listing.md) for the provider-specific parameters and requirements.

