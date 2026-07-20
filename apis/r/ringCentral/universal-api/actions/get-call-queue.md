# RingCentral: Get Call Queue

Retrieves a call queue from a RingCentral account.

```
GET https://connect.mindcloud.co/v1/universal/ringCentral/latest/actions/get-call-queue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RingCentral `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ringCentral/latest/actions/get-call-queue?connectionId=$CONNECTION_ID&accountId=string&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string",
  "groupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ringCentral/latest/actions/get-call-queue?${params}`, {
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
| `accountId` | string | yes |  |
| `groupId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "extensionNumber": "string",
      "id": "string",
      "members": [
        {}
      ],
      "name": "Ava Chen",
      "type": "string",
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `extensionNumber` | string |  |
| `id` | string |  |
| `members` | array<object> |  |
| `name` | string |  |
| `type` | string |  |
| `uri` | string |  |

## Native endpoint

Through the native RingCentral API, this operation is `GET restapi/v1.0/account/:accountId/call-queues/:groupId` (base URL `https://platform.ringcentral.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-call-queue.md) for the provider-specific parameters and requirements.

