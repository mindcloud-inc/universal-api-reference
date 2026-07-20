# Cloze: Add Communication Record

Creates a communication record in Cloze.

```
POST https://connect.mindcloud.co/v1/universal/cloze/latest/actions/add-communication-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloze/latest/actions/add-communication-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloze/latest/actions/add-communication-record', {
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
| `date` | string | no | When the communication happened. Example: `2026-03-18T18:18:00Z`. |
| `bodytype` | string | no | Type of the body. Example: `text`. |
| `style` | string | no | Style of the communication. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`. |
| `from` | string | no | Address of the person initiating the communication. |
| `recipients[]` | array<object> | no | Recipients or attendees for the communication. |
| `recipients[].value` | string | no | Identifier for the recipient. |
| `subject` | string | no | Subject of the communication. |
| `body` | string | no | Body text of the communication. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorcode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorcode` | number |  |

## Native endpoint

Through the native Cloze API, this operation is `POST /v1/timeline/communication/create` (base URL `https://api.cloze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-communication-record.md) for the provider-specific parameters and requirements.

