# Bokun: List Promo Codes

Retrieves promo codes from the current Bokun vendor.

```
GET https://connect.mindcloud.co/v1/universal/bokun/latest/actions/list-promo-codes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bokun `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bokun/latest/actions/list-promo-codes?connectionId=$CONNECTION_ID&pageNo=1&pageSize=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pageNo": "1",
  "pageSize": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bokun/latest/actions/list-promo-codes?${params}`, {
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
| `pageNo` | number | yes | The page number to fetch. Default: `1`. |
| `pageSize` | number | yes | The number of records to fetch per page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {}
      ],
      "pageNo": 1,
      "pageSize": 1,
      "totalCount": 1,
      "totalPageCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> |  |
| `pageNo` | number |  |
| `pageSize` | number |  |
| `totalCount` | number |  |
| `totalPageCount` | number |  |

## Native endpoint

Through the native Bokun API, this operation is `GET /restapi/v2.0/promo/codes` (base URL `https://api.bokun.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-promo-codes.md) for the provider-specific parameters and requirements.

