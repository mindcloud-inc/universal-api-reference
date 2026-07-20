# turboSMTP: List Validated Emails by List

Retrieves validated emails from a turboSMTP validation list.

```
GET https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/list-validated-emails-by-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a turboSMTP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/list-validated-emails-by-list?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/list-validated-emails-by-list?${params}`, {
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
      "count": 1,
      "processed": 1,
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `processed` | number |  |
| `results` | array<object> |  |

## Native endpoint

Through the native turboSMTP API, this operation is `GET /emailvalidation/lists/{Id}/emails` (base URL `https://pro.api.serversmtp.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-validated-emails-by-list.md) for the provider-specific parameters and requirements.

