# ironSource: Create Placements

Creates new placements in ironSource.

```
POST https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/create-placements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ironSource `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/create-placements" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/create-placements', {
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
| `appKey` | string | no | Application key to create placements for. |
| `placements` | string | no | Array of placement objects to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appKey": "string",
      "placements": [
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
| `appKey` | string | Application unique identifier. |
| `placements` | array<object> | Created placement rows containing adUnit, id, and name. |

## Native endpoint

Through the native ironSource API, this operation is `POST partners/publisher/placements/v1` (base URL `https://platform.ironsrc.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-placements.md) for the provider-specific parameters and requirements.

