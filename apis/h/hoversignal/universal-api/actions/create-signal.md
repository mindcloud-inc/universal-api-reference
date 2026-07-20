# Hoversignal: Create Signal



```
POST https://connect.mindcloud.co/v1/universal/hoversignal/latest/actions/create-signal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hoversignal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hoversignal/latest/actions/create-signal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hoversignal/latest/actions/create-signal', {
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
| `name` | string | no |  |
| `type` | string | no |  |
| `iconType` | string | no |  |
| `order` | number | no |  |
| `displayDuration` | number | no |  |
| `frequency` | string | no |  |
| `pageFilterType` | string | no |  |
| `deviceFilter` | string | no |  |
| `isActive` | boolean | no |  |
| `isRequired` | boolean | no |  |
| `text` | string | no |  |
| `actionText` | string | no |  |
| `linkUrl` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | The created signal identifier. |
| `success` | boolean | Whether the signal was created successfully. |

## Native endpoint

Through the native Hoversignal API, this operation is `POST /api/v1/signals` (base URL `https://app.hoversignal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-signal.md) for the provider-specific parameters and requirements.

