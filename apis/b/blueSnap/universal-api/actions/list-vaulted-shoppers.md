# BlueSnap: List Vaulted Shoppers

Retrieves vaulted shoppers from BlueSnap.

```
GET https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/list-vaulted-shoppers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlueSnap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/list-vaulted-shoppers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/list-vaulted-shoppers?${params}`, {
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
      "lastPage": true,
      "shoppers": [
        {
          "country": "string",
          "email": "ava@example.com",
          "firstName": "Ava",
          "lastName": "Chen",
          "shopperCurrency": "string",
          "vaultedShopperId": 1
        }
      ],
      "totalResults": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `lastPage` | boolean | Whether this is the last page. |
| `shoppers[].country` | string | Country code. |
| `shoppers[].email` | string | Email address. |
| `shoppers[].firstName` | string | First name. |
| `shoppers[].lastName` | string | Last name. |
| `shoppers[].shopperCurrency` | string | Shopper currency. |
| `shoppers[].vaultedShopperId` | number | Vaulted shopper ID. |
| `totalResults` | number | Total results count. |

## Native endpoint

Through the native BlueSnap API, this operation is `GET /vaulted-shoppers` (base URL `https://sandbox.bluesnap.com/services/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-vaulted-shoppers.md) for the provider-specific parameters and requirements.

