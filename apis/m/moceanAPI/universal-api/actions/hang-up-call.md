# Mocean API: Hang Up Call



```
PUT https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/hang-up-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mocean API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/hang-up-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "callUuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/hang-up-call', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "callUuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `callUuid` | string | yes | The call UUID to hang up. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "calls": [
        {
          "id": "string",
          "status": "string"
        }
      ],
      "error": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calls[].id` | string |  |
| `calls[].status` | string |  |
| `error` | string |  |

## Native endpoint

Through the native Mocean API API, this operation is `POST /rest/2/voice/hangup?mocean-resp-format=json` (base URL `https://rest.moceanapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/hang-up-call.md) for the provider-specific parameters and requirements.

