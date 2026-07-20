# Loop & Tie: Bulk Create Gifts

Creates multiple gifts at once in Loop & Tie.

```
POST https://connect.mindcloud.co/v1/universal/loopTie/latest/actions/bulk-create-gifts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loop & Tie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/loopTie/latest/actions/bulk-create-gifts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loopTie/latest/actions/bulk-create-gifts', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | string | no | The Loop & Tie team ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "included": [
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
| `data` | array<object> | The created bulk gift records. |
| `included` | array<object> | Related sender, collection, logo, and design records. |

## Native endpoint

Through the native Loop & Tie API, this operation is `POST /teams/:teamId/bulk/gifts` (base URL `https://api.loopandtie.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-create-gifts.md) for the provider-specific parameters and requirements.

