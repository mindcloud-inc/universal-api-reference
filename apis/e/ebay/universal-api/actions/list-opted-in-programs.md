# eBay: List Opted-In Programs

Retrieve a list of the seller programs that the authenticated seller has opted-in to.

```
GET https://connect.mindcloud.co/v1/universal/ebay/latest/actions/list-opted-in-programs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eBay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ebay/latest/actions/list-opted-in-programs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ebay/latest/actions/list-opted-in-programs?${params}`, {
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
      "programType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `programType` | string |  |

## Native endpoint

Through the native eBay API, this operation is `GET sell/account/v1/program/get_opted_in_programs` (base URL `https://api.ebay.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-opted-in-programs.md) for the provider-specific parameters and requirements.

