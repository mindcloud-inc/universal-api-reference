# GenderAPI.io: Get Remaining Credits

Retrieves remaining API credits from GenderAPI.io.

```
GET https://connect.mindcloud.co/v1/universal/genderAPIio/latest/actions/get-remaining-credits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GenderAPI.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/genderAPIio/latest/actions/get-remaining-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/genderAPIio/latest/actions/get-remaining-credits?${params}`, {
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
      "expiresAt": 1,
      "remaining": 1,
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expiresAt` | number | Unix timestamp for the current credit package expiration. |
| `remaining` | number | The number of API credits remaining. |
| `status` | boolean | Whether the quota request was successful. |

## Native endpoint

Through the native GenderAPI.io API, this operation is `GET /api/remaining` (base URL `https://api.genderapi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-remaining-credits.md) for the provider-specific parameters and requirements.

