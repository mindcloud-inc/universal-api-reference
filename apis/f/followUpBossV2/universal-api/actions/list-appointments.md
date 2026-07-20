# Follow Up Boss: List Appointments

Retrieves appointments from Follow Up Boss.

```
GET https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/list-appointments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Follow Up Boss `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/list-appointments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/list-appointments?${params}`, {
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
      "appointments": [
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
| `appointments[]` | array<object> |  |
| `appointments[].allDay` | boolean |  |
| `appointments[].created` | string |  |
| `appointments[].createdById` | number |  |
| `appointments[].description` | string |  |
| `appointments[].detailsVisible` | boolean |  |
| `appointments[].end` | string |  |
| `appointments[].externalCalendarId` | object |  |
| `appointments[].externalEventLink` | object |  |
| `appointments[].id` | number |  |
| `appointments[].invitees[]` | array<object> |  |
| `appointments[].invitees[].email` | string |  |
| `appointments[].invitees[].name` | string |  |
| `appointments[].invitees[].personId` | object |  |
| `appointments[].invitees[].picture` | object |  |
| `appointments[].invitees[].picture.original` | string |  |
| `appointments[].invitees[].picture.value162x162` | string |  |
| `appointments[].invitees[].picture.value26x26` | string |  |
| `appointments[].invitees[].picture.value30x30` | string |  |
| `appointments[].invitees[].picture.value40x40` | string |  |
| `appointments[].invitees[].picture.value60x60` | string |  |
| `appointments[].invitees[].relationshipId` | object |  |
| `appointments[].invitees[].userId` | number |  |
| `appointments[].isDeletable` | boolean |  |
| `appointments[].isEditable` | boolean |  |
| `appointments[].location` | string |  |
| `appointments[].originFub` | boolean |  |
| `appointments[].outcome` | object |  |
| `appointments[].outcomeId` | object |  |
| `appointments[].start` | string |  |
| `appointments[].timezone` | string |  |
| `appointments[].title` | string |  |
| `appointments[].type` | object |  |
| `appointments[].typeId` | object |  |
| `appointments[].updated` | string |  |
| `appointments[].updatedById` | number |  |
| `metadata` | object |  |
| `metadata.collection` | string |  |
| `metadata.limit` | number |  |
| `metadata.next` | object |  |
| `metadata.nextLink` | object |  |
| `metadata.offset` | number |  |
| `metadata.total` | number |  |

## Native endpoint

Through the native Follow Up Boss API, this operation is `GET appointments` (base URL `https://api.followupboss.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-appointments.md) for the provider-specific parameters and requirements.

