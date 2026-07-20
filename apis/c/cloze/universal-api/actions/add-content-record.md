# Cloze: Add Content Record

Creates a content record in Cloze.

```
POST https://connect.mindcloud.co/v1/universal/cloze/latest/actions/add-content-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloze/latest/actions/add-content-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloze/latest/actions/add-content-record', {
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
| `style` | string | no | Style of the content record. One of: `0`, `1`, `2`, `3`. |
| `from` | string | no | Address of the person who created the content record. |
| `uniqueid` | string | no | Unique identifier for the content record. |
| `source` | string | no | Source domain for the content record. |
| `subject` | string | no | Subject of the content record. |
| `body` | string | no | Body text of the content record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorcode": 1,
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorcode` | number | Error code. 0 means success. |
| `message` | string | Human-readable error description when the request fails. |

## Native endpoint

Through the native Cloze API, this operation is `POST /v1/timeline/content/create` (base URL `https://api.cloze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-content-record.md) for the provider-specific parameters and requirements.

