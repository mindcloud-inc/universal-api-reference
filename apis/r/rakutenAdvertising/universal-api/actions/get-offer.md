# Rakuten Advertising: Get offer

Retrieves an offer from Rakuten Advertising.

```
GET https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/get-offer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rakuten Advertising `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/get-offer?connectionId=$CONNECTION_ID&goid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "goid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/get-offer?${params}`, {
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
| `goid` | string | yes | Rakuten group offer ID from the offers API. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "advertiserId": "string",
      "advertiserName": "Ava Chen",
      "description": "string",
      "endDate": "2026-05-07T12:00:00.000Z",
      "goid": "string",
      "name": "Ava Chen",
      "network": "string",
      "offerStatus": "string",
      "offerType": "string",
      "oid": "string",
      "startDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `advertiserId` | string |  |
| `advertiserName` | string |  |
| `description` | string |  |
| `endDate` | date |  |
| `goid` | string |  |
| `name` | string |  |
| `network` | string |  |
| `offerStatus` | string |  |
| `offerType` | string |  |
| `oid` | string |  |
| `startDate` | date |  |

## Native endpoint

Through the native Rakuten Advertising API, this operation is `GET /v1/offers/{goid}` (base URL `https://api.linksynergy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-offer.md) for the provider-specific parameters and requirements.

