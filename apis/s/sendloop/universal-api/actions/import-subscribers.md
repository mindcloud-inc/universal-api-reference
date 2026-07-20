# Sendloop: Import Subscribers



```
POST https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/import-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendloop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/import-subscribers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": 1,
  "subscriber1Email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/import-subscribers', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": 1,
    "subscriber1Email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listId` | number | yes | ID of the target list to import subscribers |
| `subscriber1Email` | string | yes | First subscriber email address |

## Response

```json
{
  "success": true,
  "data": [
    {
      "totalDuplicate": 1,
      "totalFailed": 1,
      "totalImported": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `totalDuplicate` | number |  |
| `totalFailed` | number |  |
| `totalImported` | number |  |

## Native endpoint

Through the native Sendloop API, this operation is `POST /subscriber.import/json` (base URL `https://{{credentials.subdomain}}.sendloop.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-subscribers.md) for the provider-specific parameters and requirements.

