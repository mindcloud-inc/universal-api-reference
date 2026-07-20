# SMSGlobal: List Shared Pools

Retrieves shared pools from the SMSGlobal account.

```
GET https://connect.mindcloud.co/v1/universal/sMSGlobal/latest/actions/list-shared-pools
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSGlobal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSGlobal/latest/actions/list-shared-pools?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSGlobal/latest/actions/list-shared-pools?${params}`, {
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
      "SharedPools": [
        {
          "id": 1,
          "name": "Ava Chen",
          "numbers": [
            {
              "msisdn": "string"
            }
          ],
          "size": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `SharedPools[].id` | number | Shared pool identifier. |
| `SharedPools[].name` | string | Shared pool name. |
| `SharedPools[].numbers[].msisdn` | string | Mobile number in the shared pool. |
| `SharedPools[].size` | number | Number of numbers in the shared pool. |

## Native endpoint

Through the native SMSGlobal API, this operation is `GET /v2/sharedpool` (base URL `https://api.smsglobal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-shared-pools.md) for the provider-specific parameters and requirements.

