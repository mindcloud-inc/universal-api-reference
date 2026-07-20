# Rakuten Advertising: List partnerships

Retrieves partnerships from Rakuten Advertising.

```
GET https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/list-partnerships
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rakuten Advertising `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/list-partnerships?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/list-partnerships?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "advertiserId": "string",
      "advertiserName": "Ava Chen",
      "advertiserStatus": "string",
      "applyDate": "2026-05-07T12:00:00.000Z",
      "approveDate": "2026-05-07T12:00:00.000Z",
      "network": "string",
      "partnerStatus": "string",
      "statusUpdatedAt": "2026-05-07T12:00:00.000Z"
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
| `advertiserStatus` | string |  |
| `applyDate` | date |  |
| `approveDate` | date |  |
| `network` | string |  |
| `partnerStatus` | string |  |
| `statusUpdatedAt` | date |  |

## Native endpoint

Through the native Rakuten Advertising API, this operation is `GET /v1/partnerships` (base URL `https://api.linksynergy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-partnerships.md) for the provider-specific parameters and requirements.

