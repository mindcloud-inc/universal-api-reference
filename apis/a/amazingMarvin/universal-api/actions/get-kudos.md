# Amazing Marvin: Get Kudos

Retrieves kudos information from Amazing Marvin.

```
GET https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/get-kudos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazing Marvin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/get-kudos?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/get-kudos?${params}`, {
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
      "kudos": 1,
      "kudosRemaining": 1,
      "level": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `kudos` | number |  |
| `kudosRemaining` | number |  |
| `level` | number |  |

## Native endpoint

Through the native Amazing Marvin API, this operation is `GET /kudos` (base URL `https://serv.amazingmarvin.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-kudos.md) for the provider-specific parameters and requirements.

