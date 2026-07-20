# SelectPdf: Get API Usage



```
GET https://connect.mindcloud.co/v1/universal/selectPdf/latest/actions/get-api-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SelectPdf `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/selectPdf/latest/actions/get-api-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/selectPdf/latest/actions/get-api-usage?${params}`, {
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
| `getHistory` | boolean | no | Include monthly conversion history in the response. Default: `False`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "available": 1,
      "history": [
        {}
      ],
      "limit": 1,
      "status": "string",
      "subscriptionType": "string",
      "used": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `available` | number | Conversions still available. |
| `history` | array<object> | Monthly usage history entries when requested. |
| `limit` | number | Monthly conversion limit for the license. |
| `status` | string | License status message returned by SelectPdf. |
| `subscriptionType` | string | The active SelectPdf subscription tier. |
| `used` | number | Conversions already used. |

## Native endpoint

Through the native SelectPdf API, this operation is `GET /usage/` (base URL `https://selectpdf.com/api2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-usage.md) for the provider-specific parameters and requirements.

