# CallRail: Get Account

Retrieves an account from CallRail.

```
GET https://connect.mindcloud.co/v1/universal/callRail/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallRail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callRail/latest/actions/get-account?connectionId=$CONNECTION_ID&account_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "account_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callRail/latest/actions/get-account?${params}`, {
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
| `account_id` | string | yes | The CallRail account ID. |
| `fields` | string | no | Comma-separated additional account fields to include in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agencyInTrial": true,
      "brandStatus": "string",
      "createdAt": "string",
      "hasZuoraAccount": true,
      "hipaaAccount": true,
      "id": "string",
      "inboundRecordingEnabled": true,
      "name": "Ava Chen",
      "numericId": 1,
      "outboundRecordingEnabled": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agencyInTrial` | boolean |  |
| `brandStatus` | string |  |
| `createdAt` | string |  |
| `hasZuoraAccount` | boolean |  |
| `hipaaAccount` | boolean |  |
| `id` | string |  |
| `inboundRecordingEnabled` | boolean |  |
| `name` | string |  |
| `numericId` | number |  |
| `outboundRecordingEnabled` | boolean |  |

## Native endpoint

Through the native CallRail API, this operation is `GET /v3/a/:account_id.json` (base URL `https://api.callrail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

