# Swipe One: List Contact Events



```
GET https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/list-contact-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swipe One `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/list-contact-events?connectionId=$CONNECTION_ID&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/list-contact-events?${params}`, {
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
| `contactId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "count": 1,
        "events": [
          {
            "contactId": "string",
            "createdAt": "string",
            "createdBy": {
              "id": "string",
              "name": "Ava Chen",
              "type": "string"
            },
            "properties": {
              "tag": "string",
              "tags": {
                "from": [
                  "string"
                ],
                "to": [
                  "string"
                ]
              }
            },
            "type": "string",
            "workspaceId": "string"
          }
        ],
        "page": 1,
        "source": "string"
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.count` | number |  |
| `data.events[].contactId` | string |  |
| `data.events[].createdAt` | string |  |
| `data.events[].createdBy.id` | string |  |
| `data.events[].createdBy.name` | string |  |
| `data.events[].createdBy.type` | string |  |
| `data.events[].properties.tag` | string |  |
| `data.events[].properties.tags.from[]` | string |  |
| `data.events[].properties.tags.to[]` | string |  |
| `data.events[].type` | string |  |
| `data.events[].workspaceId` | string |  |
| `data.page` | number |  |
| `data.source` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Swipe One API, this operation is `GET /contacts/:contactId/events` (base URL `https://api.swipeone.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-events.md) for the provider-specific parameters and requirements.

