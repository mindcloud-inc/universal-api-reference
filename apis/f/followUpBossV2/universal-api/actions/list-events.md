# Follow Up Boss: List Events

Retrieves events from Follow Up Boss.

```
GET https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Follow Up Boss `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/list-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/list-events?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "events": [
        [
          {}
        ]
      ],
      "metadata": {
        "collection": "string",
        "limit": 1,
        "next": {},
        "nextLink": {},
        "offset": 1,
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `events[]` | array<object> |  |
| `events[].additional[]` | array<string> |  |
| `events[].created` | string |  |
| `events[].description` | string |  |
| `events[].id` | number |  |
| `events[].message` | string |  |
| `events[].noteId` | object |  |
| `events[].occurred` | string |  |
| `events[].pageDuration` | number |  |
| `events[].pageTitle` | object |  |
| `events[].pageUrl` | object |  |
| `events[].personId` | number |  |
| `events[].property` | object |  |
| `events[].propertySearch` | object |  |
| `events[].source` | string |  |
| `events[].type` | string |  |
| `events[].updated` | string |  |
| `metadata` | object |  |
| `metadata.collection` | string |  |
| `metadata.limit` | number |  |
| `metadata.next` | object |  |
| `metadata.nextLink` | object |  |
| `metadata.offset` | number |  |
| `metadata.total` | number |  |

## Native endpoint

Through the native Follow Up Boss API, this operation is `GET events` (base URL `https://api.followupboss.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

