# Gorgias: Retrieve Survey

Retrieves a satisfaction survey from Gorgias.

```
GET https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-survey
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gorgias `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-survey?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-survey?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Survey ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body_text": "string",
      "created_datetime": "string",
      "customer_id": 1,
      "id": 1,
      "meta": {},
      "score": 1,
      "scored_datetime": "string",
      "sent_datetime": "string",
      "should_send_datetime": "string",
      "ticket_id": 1,
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body_text` | string |  |
| `created_datetime` | string |  |
| `customer_id` | number |  |
| `id` | number |  |
| `meta` | object |  |
| `score` | number |  |
| `scored_datetime` | string |  |
| `sent_datetime` | string |  |
| `should_send_datetime` | string |  |
| `ticket_id` | number |  |
| `uri` | string |  |

## Native endpoint

Through the native Gorgias API, this operation is `GET /surveys/:id` (base URL `https://{{credentials.subdomain}}.gorgias.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-survey.md) for the provider-specific parameters and requirements.

