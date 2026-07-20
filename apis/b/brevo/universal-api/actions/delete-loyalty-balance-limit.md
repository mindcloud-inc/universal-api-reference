# Brevo: Delete Loyalty Balance Limit



```
DELETE https://connect.mindcloud.co/v1/universal/brevo/latest/actions/delete-loyalty-balance-limit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brevo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/brevo/latest/actions/delete-loyalty-balance-limit?connectionId=$CONNECTION_ID&bdid=string&blid=string&pid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bdid": "string",
  "blid": "string",
  "pid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brevo/latest/actions/delete-loyalty-balance-limit?${params}`, {
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
| `bdid` | string | yes |  |
| `blid` | string | yes |  |
| `pid` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Brevo API, this operation is `DELETE /v3/loyalty/balance/programs/:pid/balance-definitions/:bdid/limits/:blid` (base URL `https://api.brevo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-loyalty-balance-limit.md) for the provider-specific parameters and requirements.

