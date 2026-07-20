# Billetto: List Event Campaigns

Retrieves campaigns for an event from Billetto.

```
GET https://connect.mindcloud.co/v1/universal/billetto/latest/actions/list-event-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billetto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billetto/latest/actions/list-event-campaigns?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billetto/latest/actions/list-event-campaigns?${params}`, {
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
| `id` | string | yes | Billetto event ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "has_more": true,
      "object": "string",
      "total": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `has_more` | boolean |  |
| `object` | string |  |
| `total` | number |  |
| `url` | string |  |

## Native endpoint

Through the native Billetto API, this operation is `GET organiser/events/{id}/campaigns` (base URL `https://billetto.dk/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-event-campaigns.md) for the provider-specific parameters and requirements.

