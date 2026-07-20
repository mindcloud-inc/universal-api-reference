# SMSGlobal: List Opt-Outs

Retrieves opted-out numbers from the SMSGlobal account.

```
GET https://connect.mindcloud.co/v1/universal/sMSGlobal/latest/actions/list-opt-outs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSGlobal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSGlobal/latest/actions/list-opt-outs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSGlobal/latest/actions/list-opt-outs?${params}`, {
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
      "limit": 1,
      "offset": 1,
      "optouts": [
        {
          "number": "string",
          "status": "string"
        }
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `limit` | number | Number of opt-out rows returned. |
| `offset` | number | Pagination offset. |
| `optouts[].number` | string | Opted-out mobile number. |
| `optouts[].status` | string | Opt-out validation status. |
| `total` | number | Total number of opt-out rows. |

## Native endpoint

Through the native SMSGlobal API, this operation is `GET /v2/opt-outs` (base URL `https://api.smsglobal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-opt-outs.md) for the provider-specific parameters and requirements.

