# Rakuten Advertising: Get merchants by application status

Retrieves merchants from Rakuten Advertising by application status.

```
GET https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/get-merchants-by-application-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rakuten Advertising `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/get-merchants-by-application-status?connectionId=$CONNECTION_ID&applicationStatus=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "applicationStatus": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/get-merchants-by-application-status?${params}`, {
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
| `applicationStatus` | string | yes | Advertiser application status to filter merchants. |

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

Through the native Rakuten Advertising API, this operation is `GET /linklocator/1.0/getMerchByAppStatus/{applicationStatus}` (base URL `https://api.linksynergy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-merchants-by-application-status.md) for the provider-specific parameters and requirements.

