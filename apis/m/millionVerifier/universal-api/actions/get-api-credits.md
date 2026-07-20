# MillionVerifier: Get API Credits

Retrieves available API credits from MillionVerifier.

```
GET https://connect.mindcloud.co/v1/universal/millionVerifier/latest/actions/get-api-credits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MillionVerifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/millionVerifier/latest/actions/get-api-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/millionVerifier/latest/actions/get-api-credits?${params}`, {
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
      "bulkCredits": 1,
      "credits": 1,
      "plan": 1,
      "renewingCredits": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bulkCredits` | number |  |
| `credits` | number |  |
| `plan` | number |  |
| `renewingCredits` | number |  |

## Native endpoint

Through the native MillionVerifier API, this operation is `GET /api/v3/credits` (base URL `https://api.millionverifier.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-credits.md) for the provider-specific parameters and requirements.

