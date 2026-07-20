# RegFox: List Global Coupons

Retrieves global coupons from the RegFox account.

```
GET https://connect.mindcloud.co/v1/universal/regFox/latest/actions/list-global-coupons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RegFox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/regFox/latest/actions/list-global-coupons?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/regFox/latest/actions/list-global-coupons?${params}`, {
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
      "data": [
        {}
      ],
      "responseCode": 1,
      "totalResults": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Global coupons returned for the authenticated RegFox account. |
| `responseCode` | number | HTTP-style response code returned by Webconnex. |
| `totalResults` | number | Total number of matching global coupons. |

## Native endpoint

Through the native RegFox API, this operation is `GET coupons/global` (base URL `https://api.webconnex.com/v2/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-global-coupons.md) for the provider-specific parameters and requirements.

