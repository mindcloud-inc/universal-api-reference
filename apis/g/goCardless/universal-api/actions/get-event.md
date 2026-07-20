# GoCardless: Get Event

Retrieves a single event from GoCardless.

```
GET https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/get-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCardless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/get-event?connectionId=$CONNECTION_ID&identity=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identity": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/get-event?${params}`, {
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
| `identity` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "events": {
        "action": "string",
        "createdAt": "string",
        "details": {
          "cause": "string",
          "description": "string",
          "origin": "string"
        },
        "id": "string",
        "links": {
          "payment": "https://example.com"
        },
        "resourceType": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `events.action` | string |  |
| `events.createdAt` | string |  |
| `events.details.cause` | string |  |
| `events.details.description` | string |  |
| `events.details.origin` | string |  |
| `events.id` | string |  |
| `events.links.payment` | string |  |
| `events.resourceType` | string |  |

## Native endpoint

Through the native GoCardless API, this operation is `GET /events/:identity` (base URL `https://api-sandbox.gocardless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event.md) for the provider-specific parameters and requirements.

