# Nvoip: List Scheduled SMS



```
GET https://connect.mindcloud.co/v1/universal/nvoip/latest/actions/list-scheduled-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nvoip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nvoip/latest/actions/list-scheduled-sms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nvoip/latest/actions/list-scheduled-sms?${params}`, {
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
      "id": "string",
      "message": "string",
      "schedulingDate": "string",
      "toNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Scheduled SMS identifier. |
| `message` | string | Scheduled SMS content. |
| `schedulingDate` | string | Scheduled delivery datetime. |
| `toNumber` | string | Destination number. |

## Native endpoint

Through the native Nvoip API, this operation is `GET /list/sched/torpedo` (base URL `https://api.nvoip.com.br/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-scheduled-sms.md) for the provider-specific parameters and requirements.

