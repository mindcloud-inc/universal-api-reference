# Vaiz: Add Reaction

Adds a reaction to a comment in Vaiz.

```
POST https://connect.mindcloud.co/v1/universal/vaiz/latest/actions/add-reaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vaiz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vaiz/latest/actions/add-reaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vaiz/latest/actions/add-reaction', {
  method: 'POST',
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "reactions": [
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
| `reactions` | array<object> |  |

## Native endpoint

Through the native Vaiz API, this operation is `POST reactToComment` (base URL `https://api.vaiz.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-reaction.md) for the provider-specific parameters and requirements.

