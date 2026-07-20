# EventSquare: Get Make Account

Retrieves the connected Make account from EventSquare.

```
GET https://connect.mindcloud.co/v1/universal/eventSquare/latest/actions/get-make-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EventSquare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventSquare/latest/actions/get-make-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventSquare/latest/actions/get-make-account?${params}`, {
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
      "account": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | string | The EventSquare account name returned when the API key is valid. |

## Native endpoint

Through the native EventSquare API, this operation is `GET /1.0/integrations/make/test` (base URL `https://api.eventsquare.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-make-account.md) for the provider-specific parameters and requirements.

