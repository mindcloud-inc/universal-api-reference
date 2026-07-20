# OptiMonk: Get Account

Retrieves account details from OptiMonk.

```
GET https://connect.mindcloud.co/v1/universal/optiMonk/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OptiMonk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/optiMonk/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/optiMonk/latest/actions/get-account?${params}`, {
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
      "remainingPageView": 1,
      "remainingVisitor": 1,
      "usedPageView": 1,
      "usedVisitor": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `remainingPageView` | number |  |
| `remainingVisitor` | number |  |
| `usedPageView` | number |  |
| `usedVisitor` | number |  |

## Native endpoint

Through the native OptiMonk API, this operation is `GET /account/` (base URL `https://api.optimonk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

