# Let's Calendar: List Campaign Attendees

Retrieves campaign attendees from Let's Calendar.

```
GET https://connect.mindcloud.co/v1/universal/letsCalendar/latest/actions/list-campaign-attendees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Let's Calendar `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/letsCalendar/latest/actions/list-campaign-attendees?connectionId=$CONNECTION_ID&limit=25&offset=0&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/letsCalendar/latest/actions/list-campaign-attendees?${params}`, {
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
| `campaignId` | string | yes | The unique identifier of the campaign to get attendees from. |
| `status` | string | no | Filter by attendee status: N, S, F, U, P, or C. |
| `source` | string | no | Filter by attendee source such as zapier, api, import, manual, copy, zoom, Public URL, or test-invite. |
| `registeredFrom` | string | no | Filter attendees registered from this date in Y-m-d format. |
| `registeredTo` | string | no | Filter attendees registered to this date in Y-m-d format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attendees": {
        "currentPage": 1,
        "data": [
          {
            "email": "ava@example.com",
            "id": 1,
            "loginUrl": "https://example.com",
            "name": "Ava Chen",
            "password": "string",
            "registeredAt": "string",
            "source": "string",
            "status": "string",
            "statusLabel": "string",
            "username": "Ava Chen"
          }
        ],
        "perPage": 1,
        "total": 1
      },
      "summary": {
        "campaignId": "string",
        "campaignName": "Ava Chen",
        "cancelledContacts": 1,
        "failedContacts": 1,
        "inprocessContacts": 1,
        "newContacts": 1,
        "sentContacts": 1,
        "totalContacts": 1,
        "unsubscribeContacts": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attendees.currentPage` | number |  |
| `attendees.data[].email` | string |  |
| `attendees.data[].id` | number |  |
| `attendees.data[].loginUrl` | string |  |
| `attendees.data[].name` | string |  |
| `attendees.data[].password` | string |  |
| `attendees.data[].registeredAt` | string |  |
| `attendees.data[].source` | string |  |
| `attendees.data[].status` | string |  |
| `attendees.data[].statusLabel` | string |  |
| `attendees.data[].username` | string |  |
| `attendees.perPage` | number |  |
| `attendees.total` | number |  |
| `summary.campaignId` | string |  |
| `summary.campaignName` | string |  |
| `summary.cancelledContacts` | number |  |
| `summary.failedContacts` | number |  |
| `summary.inprocessContacts` | number |  |
| `summary.newContacts` | number |  |
| `summary.sentContacts` | number |  |
| `summary.totalContacts` | number |  |
| `summary.unsubscribeContacts` | number |  |

## Native endpoint

Through the native Let's Calendar API, this operation is `GET campaign/:campaignId/attendees` (base URL `https://panel.letscalendar.com/api/lc`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-campaign-attendees.md) for the provider-specific parameters and requirements.

