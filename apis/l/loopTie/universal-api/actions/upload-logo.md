# Loop & Tie: Upload Logo

Creates a new logo in Loop & Tie.

```
POST https://connect.mindcloud.co/v1/universal/loopTie/latest/actions/upload-logo
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loop & Tie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/loopTie/latest/actions/upload-logo" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loopTie/latest/actions/upload-logo', {
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
| `logoImageUrl` | string | no | Public image URL for the logo. |
| `logoName` | string | no | Display name for the logo. |
| `teamId` | string | no | The Loop & Tie team ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | The uploaded logo record. |

## Native endpoint

Through the native Loop & Tie API, this operation is `POST /teams/:teamId/logos` (base URL `https://api.loopandtie.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-logo.md) for the provider-specific parameters and requirements.

