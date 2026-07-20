# MyEmailVerifier: Get Credits

Retrieves remaining verification credits from MyEmailVerifier.

```
GET https://connect.mindcloud.co/v1/universal/myEmailVerifier/latest/actions/get-credits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MyEmailVerifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/myEmailVerifier/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/myEmailVerifier/latest/actions/get-credits?${params}`, {
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
      "credits": 1,
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits` | number | Remaining verification credits available on the account. |
| `status` | boolean | Whether the credits lookup succeeded. |

## Native endpoint

Through the native MyEmailVerifier API, this operation is `GET /verifier/getcredits/{{credentials.apiKey}}` (base URL `https://client.myemailverifier.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-credits.md) for the provider-specific parameters and requirements.

