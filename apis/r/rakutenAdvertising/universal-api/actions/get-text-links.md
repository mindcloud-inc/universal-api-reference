# Rakuten Advertising: Get text links

Retrieves text links from Rakuten Advertising.

```
GET https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/get-text-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rakuten Advertising `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/get-text-links?connectionId=$CONNECTION_ID&advertiserId=string&campaignId=0&categoryId=string&linkEndDate=https%3A%2F%2Fexample.com&linkStartDate=https%3A%2F%2Fexample.com&page=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "advertiserId": "string",
  "campaignId": "0",
  "categoryId": "string",
  "linkEndDate": "https://example.com",
  "linkStartDate": "https://example.com",
  "page": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/get-text-links?${params}`, {
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
| `advertiserId` | string | yes | Rakuten advertiser ID. |
| `campaignId` | string | yes | Deprecated Rakuten campaign ID path slot; use 0 when no value is required. Default: `0`. |
| `categoryId` | string | yes | Creative category ID. |
| `linkEndDate` | string | yes | End date for link availability in the format expected by Rakuten Link Locator. |
| `linkStartDate` | string | yes | Start date for link availability in the format expected by Rakuten Link Locator. |
| `page` | number | yes | Page number. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "advertiserId": "string",
      "advertiserName": "Ava Chen",
      "categoryId": "string",
      "endDate": "2026-05-07T12:00:00.000Z",
      "linkId": "https://example.com",
      "name": "Ava Chen",
      "rawXml": "string",
      "startDate": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
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
| `categoryId` | string |  |
| `endDate` | date |  |
| `linkId` | string |  |
| `name` | string |  |
| `rawXml` | string |  |
| `startDate` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Rakuten Advertising API, this operation is `GET /linklocator/1.0/getTextLinks/{advertiserId}/{categoryId}/{linkStartDate}/{linkEndDate}/{campaignId}/{page}` (base URL `https://api.linksynergy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-text-links.md) for the provider-specific parameters and requirements.

