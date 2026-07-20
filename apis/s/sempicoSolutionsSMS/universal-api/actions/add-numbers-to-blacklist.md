# Sempico Solutions SMS: Add Numbers to Blacklist



```
POST https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/add-numbers-to-blacklist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sempico Solutions SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/add-numbers-to-blacklist" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "numbers[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/add-numbers-to-blacklist', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "numbers[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `numbers[]` | array<string> | yes | Phone numbers to add to the personal blacklist. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blacklistDetails": {
        "countAfter": 1,
        "countBefore": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blacklistDetails.countAfter` | number | Blacklist count after adding numbers. |
| `blacklistDetails.countBefore` | number | Blacklist count before adding numbers. |

## Native endpoint

Through the native Sempico Solutions SMS API, this operation is `POST /black-list-add` (base URL `https://restapi.sempico.solutions/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-numbers-to-blacklist.md) for the provider-specific parameters and requirements.

