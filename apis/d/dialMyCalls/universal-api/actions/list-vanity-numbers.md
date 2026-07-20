# DialMyCalls: List Vanity Numbers

Retrieves available vanity numbers from DialMyCalls.

```
GET https://connect.mindcloud.co/v1/universal/dialMyCalls/latest/actions/list-vanity-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DialMyCalls `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dialMyCalls/latest/actions/list-vanity-numbers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dialMyCalls/latest/actions/list-vanity-numbers?${params}`, {
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
      "id": "string",
      "is10dlc": true,
      "isFree": true,
      "isLongcode": true,
      "isTcrRegistered": true,
      "nextBillDate": "2026-05-07T12:00:00.000Z",
      "nickname": "Ava Chen",
      "phone": "string",
      "status": "string",
      "tpm": 1,
      "useAsCallerid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Vanity number ID. |
| `is10dlc` | boolean | Whether this number is 10DLC-enabled. |
| `isFree` | boolean | Whether the number is marked free in DialMyCalls. |
| `isLongcode` | boolean | Whether this is a long code number. |
| `isTcrRegistered` | boolean | Whether TCR registration is complete. |
| `nextBillDate` | date | Next billing date. |
| `nickname` | string | Nickname in DialMyCalls. |
| `phone` | string | Phone number. |
| `status` | string | Current status. |
| `tpm` | number | Texts per minute limit. |
| `useAsCallerid` | boolean | Whether it may be used as caller ID. |

## Native endpoint

Through the native DialMyCalls API, this operation is `GET /vanitynumbers` (base URL `https://{{credentials.apiKey}}@api.dialmycalls.com/2.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-vanity-numbers.md) for the provider-specific parameters and requirements.

