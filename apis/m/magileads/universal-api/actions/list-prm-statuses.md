# Magileads: List PRM Statuses

Retrieves your PRM statuses from Magileads.

```
GET https://connect.mindcloud.co/v1/universal/magileads/latest/actions/list-prm-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Magileads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/magileads/latest/actions/list-prm-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/magileads/latest/actions/list-prm-statuses?${params}`, {
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
      "state": true,
      "status": [
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
| `state` | boolean |  |
| `status` | array<object> |  |

## Native endpoint

Through the native Magileads API, this operation is `GET /prm/status` (base URL `https://app.api-magileads.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-prm-statuses.md) for the provider-specific parameters and requirements.

