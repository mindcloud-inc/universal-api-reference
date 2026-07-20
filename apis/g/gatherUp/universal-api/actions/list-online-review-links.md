# GatherUp: List Online Review Links

Retrieves online review links from GatherUp.

```
GET https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/list-online-review-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatherUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/list-online-review-links?connectionId=$CONNECTION_ID&businessId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "businessId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/list-online-review-links?${params}`, {
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
| `businessId` | number | yes | Business id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "errorCode": 1,
      "errorMessage": "string",
      "OnlineReviewLinkShow": "https://example.com",
      "OnlineReviewLinkType": "https://example.com",
      "OnlineReviewLinkUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `errorCode` | number |  |
| `errorMessage` | string |  |
| `OnlineReviewLinkShow` | string |  |
| `OnlineReviewLinkType` | string |  |
| `OnlineReviewLinkUrl` | string |  |

## Native endpoint

Through the native GatherUp API, this operation is `POST /business/online-review-links/get` (base URL `https://app.gatherup.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-online-review-links.md) for the provider-specific parameters and requirements.

