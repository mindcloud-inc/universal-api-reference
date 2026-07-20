# LightwaveRF Heating: Batch Write Heating Features

Updates multiple heating features in LightwaveRF Heating.

```
PUT https://connect.mindcloud.co/v1/universal/lightwaveRFHeating/latest/actions/batch-write-heating-features
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LightwaveRF Heating `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lightwaveRFHeating/latest/actions/batch-write-heating-features" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "features[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lightwaveRFHeating/latest/actions/batch-write-heating-features', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "features[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `features[]` | array<object> | yes | The list of heating feature writes to apply in one request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "features": [
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
| `features` | array<object> | Feature write responses. |

## Native endpoint

Through the native LightwaveRF Heating API, this operation is `POST /v1/features/write` (base URL `https://publicapi.lightwaverf.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-write-heating-features.md) for the provider-specific parameters and requirements.

