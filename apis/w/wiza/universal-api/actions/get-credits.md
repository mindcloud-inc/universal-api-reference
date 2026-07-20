# Wiza: Get Credits

Retrieves your remaining Wiza credits.

```
GET https://connect.mindcloud.co/v1/universal/wiza/latest/actions/get-credits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wiza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wiza/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wiza/latest/actions/get-credits?${params}`, {
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
      "credits": {
        "apiCredits": 1,
        "emailCredits": "ava@example.com",
        "exportCredits": 1,
        "phoneCredits": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits.apiCredits` | number | Remaining API credits. |
| `credits.emailCredits` | string | Remaining email credits or the string 'unlimited'. |
| `credits.exportCredits` | number | Remaining export credits. |
| `credits.phoneCredits` | number | Remaining phone credits. |

## Native endpoint

Through the native Wiza API, this operation is `GET /meta/credits` (base URL `https://wiza.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-credits.md) for the provider-specific parameters and requirements.

