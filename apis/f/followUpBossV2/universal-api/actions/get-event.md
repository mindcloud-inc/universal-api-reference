# Follow Up Boss: Get Event

Retrieves an event from Follow Up Boss.

```
GET https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/get-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Follow Up Boss `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/get-event?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/get-event?${params}`, {
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
| `id` | string | yes | The event ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "additional": [
        {}
      ],
      "created": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "message": "string",
      "noteId": 1,
      "occurred": "2026-05-07T12:00:00.000Z",
      "pageDuration": 1,
      "pageTitle": "string",
      "pageUrl": "https://example.com",
      "personId": 1,
      "property": {},
      "propertySearch": {},
      "source": "string",
      "type": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additional` | array<object> |  |
| `created` | date |  |
| `description` | string |  |
| `id` | number |  |
| `message` | string |  |
| `noteId` | number |  |
| `occurred` | date |  |
| `pageDuration` | number |  |
| `pageTitle` | string |  |
| `pageUrl` | string |  |
| `personId` | number |  |
| `property` | object |  |
| `propertySearch` | object |  |
| `source` | string |  |
| `type` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native Follow Up Boss API, this operation is `GET events/:id` (base URL `https://api.followupboss.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event.md) for the provider-specific parameters and requirements.

