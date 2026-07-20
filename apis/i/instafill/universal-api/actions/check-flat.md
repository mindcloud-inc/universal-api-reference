# Instafill: Check Flat PDF



```
POST https://connect.mindcloud.co/v1/universal/instafill/latest/actions/check-flat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instafill `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/instafill/latest/actions/check-flat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instafill/latest/actions/check-flat', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes |  |
| `payload` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "field_count": 1,
      "is_flat": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `field_count` | number |  |
| `is_flat` | boolean |  |

## Native endpoint

Through the native Instafill API, this operation is `POST /v1/utils/check-flat` (base URL `https://api.instafill.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-flat.md) for the provider-specific parameters and requirements.

