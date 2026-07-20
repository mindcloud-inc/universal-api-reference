# Conexteo: Create Manual Stop

Creates a manual stop in Conexteo.

```
POST https://connect.mindcloud.co/v1/universal/conexteo/latest/actions/create-manual-stop
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conexteo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/conexteo/latest/actions/create-manual-stop" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "recipient": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/conexteo/latest/actions/create-manual-stop', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "recipient": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recipient` | string | yes | Phone number to add to the stop list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "recipient": "string",
      "timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Stop identifier. |
| `recipient` | string | Recipient phone number added to the stop list. |
| `timestamp` | date | Creation timestamp. |

## Native endpoint

Through the native Conexteo API, this operation is `POST /stops` (base URL `https://api.conexteo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-manual-stop.md) for the provider-specific parameters and requirements.

