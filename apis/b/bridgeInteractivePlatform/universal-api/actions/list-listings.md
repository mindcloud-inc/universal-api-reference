# Bridge Interactive Platform: List listings

Retrieves listing records from Bridge Interactive Platform.

```
GET https://connect.mindcloud.co/v1/universal/bridgeInteractivePlatform/latest/actions/list-listings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridge Interactive Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridgeInteractivePlatform/latest/actions/list-listings?connectionId=$CONNECTION_ID&dataset=test" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dataset": "test"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridgeInteractivePlatform/latest/actions/list-listings?${params}`, {
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
| `fields` | string | no | Comma-separated response fields to include. |
| `limit` | string | no | Maximum number of listings to return. |
| `offset` | string | no | Number of listings to skip before returning results. |
| `order` | string | no | Sort direction: asc or desc. |
| `sortBy` | string | no | Response field to sort listings by. |

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

Through the native Bridge Interactive Platform API, this operation is `GET /:dataset/listings` (base URL `https://api.bridgedataoutput.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-listings.md) for the provider-specific parameters and requirements.

