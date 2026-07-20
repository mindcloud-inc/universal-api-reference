# ClearoutPhone: Get Available Credits

Retrieves the available credits from ClearoutPhone.

```
GET https://connect.mindcloud.co/v1/universal/clearoutPhone/latest/actions/get-available-credits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClearoutPhone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clearoutPhone/latest/actions/get-available-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clearoutPhone/latest/actions/get-available-credits?${params}`, {
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
      "availableCredits": 1,
      "credits": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availableCredits` | number | Number of ClearoutPhone credits currently available. |
| `credits` | object | Detailed ClearoutPhone credit breakdown. |

## Native endpoint

Through the native ClearoutPhone API, this operation is `GET /phonenumber/getcredits` (base URL `https://api.clearoutphone.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-available-credits.md) for the provider-specific parameters and requirements.

