# Connecteam: List Time Clocks

Retrieve a list of time clocks associated with the account

```
GET https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/list-time-clocks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Connecteam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/list-time-clocks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/list-time-clocks?${params}`, {
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
      "id": 1,
      "isArchived": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `isArchived` | boolean |  |
| `name` | string |  |

## Native endpoint

Through the native Connecteam API, this operation is `GET /time-clock/v1/time-clocks` (base URL `https://api.connecteam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-time-clocks.md) for the provider-specific parameters and requirements.

