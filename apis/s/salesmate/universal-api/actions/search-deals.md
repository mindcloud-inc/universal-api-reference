# Salesmate: Search Deals



```
GET https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/search-deals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesmate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/search-deals?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/search-deals?${params}`, {
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
| `filterQuery` | object | no | Salesmate search filter object. Default: `{"group":{"rules":[{"data":"Jan 01, 1970 05:30 AM","field":{"type":"DateTime","fieldName":"deal.createdAt","displayName":"Created At"},"condition":"IS_AFTER","eventType":"DateTime","moduleName":"Deal"}],"operator":"AND"}}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "owner": 1,
      "status": "string",
      "statusId": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `owner` | number |  |
| `status` | string |  |
| `statusId` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Salesmate API, this operation is `POST /deal/v4/search` (base URL `https://apis.salesmate.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-deals.md) for the provider-specific parameters and requirements.

