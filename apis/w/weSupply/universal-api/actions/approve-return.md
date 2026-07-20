# WeSupply: Approve Return

Approves an existing return in WeSupply.

```
PUT https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/approve-return
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WeSupply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/approve-return" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/approve-return', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `comment` | string | no | Optional internal comment for the approval action. |
| `reference` | string | no | The WeSupply return reference to approve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native WeSupply API, this operation is `POST /returns/flow/approval/execute` (base URL `https://{{credentials.subdomain}}.labs.wesupply.xyz/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/approve-return.md) for the provider-specific parameters and requirements.

