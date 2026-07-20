# Verix: Create Multiple Credentials

Creates multiple credentials in Verix for a group.

```
POST https://connect.mindcloud.co/v1/universal/verix/latest/actions/create-multiple-credentials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/verix/latest/actions/create-multiple-credentials" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "group_id": "894",
  "inputs[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/verix/latest/actions/create-multiple-credentials', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "group_id": "894",
    "inputs[]": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `group_id` | number | yes | Target Verix group ID for credential creation. Example: `894`. |
| `issue` | boolean | no | When true, issue created credentials immediately. Example: `true`. |
| `distribute` | boolean | no | When true, distribute credentials immediately after issue. Example: `false`. |
| `inputs[]` | array<object> | yes | Array of recipient, credential, custom, and subject payload objects to create. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "requestId": 1,
      "responseQueue": [
        {
          "credentialUid": "string",
          "recipientExternalId": "string"
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
| `requestId` | number | Asynchronous Verix request identifier. |
| `responseQueue` | array<object> | Queued credential records created by the request. |
| `responseQueue[].credentialUid` | string | Credential UID queued for creation. |
| `responseQueue[].recipientExternalId` | string | Recipient external identifier. |

## Native endpoint

Through the native Verix API, this operation is `POST /v1/credentials/groups/:group_id/` (base URL `https://api.verix.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-multiple-credentials.md) for the provider-specific parameters and requirements.

