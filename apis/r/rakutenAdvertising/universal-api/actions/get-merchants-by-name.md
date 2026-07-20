# Rakuten Advertising: Get merchants by name

Finds merchants in Rakuten Advertising by name.

```
GET https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/get-merchants-by-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rakuten Advertising `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/get-merchants-by-name?connectionId=$CONNECTION_ID&advertiserName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "advertiserName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/get-merchants-by-name?${params}`, {
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
| `advertiserName` | string | yes | Advertiser name to search for in Link Locator. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "advertiserId": "string",
      "advertiserName": "Ava Chen",
      "applicationStatus": "string",
      "categoryId": "string",
      "rawXml": "string",
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
| `applicationStatus` | string |  |
| `categoryId` | string |  |
| `rawXml` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Rakuten Advertising API, this operation is `GET /linklocator/1.0/getMerchByName/{advertiserName}` (base URL `https://api.linksynergy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-merchants-by-name.md) for the provider-specific parameters and requirements.

