# Wiza: Start Individual Reveal

Starts an individual reveal in Wiza.

```
POST https://connect.mindcloud.co/v1/universal/wiza/latest/actions/start-individual-reveal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wiza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wiza/latest/actions/start-individual-reveal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "individual_reveal": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wiza/latest/actions/start-individual-reveal', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "individual_reveal": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `individual_reveal` | object | yes | Object payload describing the person to enrich. |
| `callback_url` | string | no | Webhook URL to receive async reveal updates. |
| `enrichment_level` | string | no | Optional reveal enrichment level: none, partial, phone, or full. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "id": 1,
        "is_complete": true,
        "status": "string"
      },
      "status": {
        "code": 1,
        "message": "string"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.id` | number | ID of the created individual reveal. |
| `data.is_complete` | boolean | Whether the reveal has completed. |
| `data.status` | string | Current reveal status. |
| `status.code` | number | HTTP-style status code returned by Wiza. |
| `status.message` | string | Status message from Wiza. |
| `type` | string | Response type identifier. |

## Native endpoint

Through the native Wiza API, this operation is `POST /individual_reveals` (base URL `https://wiza.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-individual-reveal.md) for the provider-specific parameters and requirements.

