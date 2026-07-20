# BunnyCDN: Get User Audit Log

Retrieves BunnyCDN user audit log entries.

```
GET https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/get-user-audit-log
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BunnyCDN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/get-user-audit-log?connectionId=$CONNECTION_ID&date=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/get-user-audit-log?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `date` | string | yes | Audit log date in Bunny route format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ContinuationToken": "string",
      "HasMoreData": true,
      "Logs": [
        {}
      ],
      "StartToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ContinuationToken` | string |  |
| `HasMoreData` | boolean |  |
| `Logs` | array<object> |  |
| `StartToken` | string |  |

## Native endpoint

Through the native BunnyCDN API, this operation is `GET /user/audit/:date` (base URL `https://api.bunny.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-audit-log.md) for the provider-specific parameters and requirements.

