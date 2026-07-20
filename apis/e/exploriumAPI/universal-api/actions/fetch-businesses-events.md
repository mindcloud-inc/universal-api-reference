# Explorium: Fetch Businesses Events

Fetches business events from Explorium API.

```
GET https://connect.mindcloud.co/v1/universal/exploriumAPI/latest/actions/fetch-businesses-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Explorium `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/exploriumAPI/latest/actions/fetch-businesses-events?connectionId=$CONNECTION_ID&business_ids%5B%5D=string&event_types%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "business_ids[]": "string",
  "event_types[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/exploriumAPI/latest/actions/fetch-businesses-events?${params}`, {
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
| `business_ids[]` | array<string> | yes | The Explorium business identifiers to query. |
| `event_types[]` | array<string> | yes | The business event types to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "responseContext": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `responseContext` | object | Explorium response metadata. |

## Native endpoint

Through the native Explorium API, this operation is `POST /v1/businesses/events` (base URL `https://api.explorium.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-businesses-events.md) for the provider-specific parameters and requirements.

