# Routee: Track multiple messages with filters for a specific time range

Tracks multiple messages with filters for a specific time range in Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/track-multiple-messages-with-filters-for-a-specific-time-range
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/track-multiple-messages-with-filters-for-a-specific-time-range?connectionId=$CONNECTION_ID&dateStart=2026-05-07T12%3A00%3A00.000Z&dateEnd=2026-05-07T12%3A00%3A00.000Z&fieldName=Ava%20Chen&searchTerm=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dateStart": "2026-05-07T12:00:00.000Z",
  "dateEnd": "2026-05-07T12:00:00.000Z",
  "fieldName": "Ava Chen",
  "searchTerm": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/track-multiple-messages-with-filters-for-a-specific-time-range?${params}`, {
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
| `dateStart` | date | yes | ISO-8601 date-time format (accept a date range only for the latest 7 days) |
| `dateEnd` | date | yes | ISO-8601 date-time format (accept a date range only for the latest 7 days) |
| `page` | number | no | The page number to retrieve, default value is 0 (meaning the first page). |
| `size` | number | no | The number of items to retrieve, default value is 20. Max value is 2000. |
| `sort` | string | no | The field name that will be used to sort the results. |
| `trackingId` | string | no | If provided then only the SMS messages for the specific Campaign Tracking Id will be retrieved. |
| `campaign` | boolean | no | If true it will return only SMS messages that belong to an SMS campaign. |
| `fieldName` | string | yes | The name of the field to filter. Available values: smsId, to, status.status, direction, label, campaign |
| `searchTerm` | string | yes | The exact value that the specified field must match. |
| `searchOperator` | string | no | Optional: The operator upon which the search operation will be executed. Possible values: 'is', 'is_not', 'contains', 'starts_with', 'ends_with'. If missing defaults to 'is'. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": [
        [
          {}
        ]
      ],
      "first": true,
      "last": true,
      "number": 1,
      "numberOfElements": 1,
      "size": 1,
      "totalElements": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content[]` | array<object> |  |
| `content[].applicationName` | string |  |
| `content[].body` | string |  |
| `content[].campaignName` | string |  |
| `content[].country` | string |  |
| `content[].direction` | string |  |
| `content[].from` | string |  |
| `content[].groups[]` | array |  |
| `content[].latency` | number |  |
| `content[].messageId` | string |  |
| `content[].operator` | string |  |
| `content[].originatingService` | string |  |
| `content[].part` | number |  |
| `content[].parts` | number |  |
| `content[].price` | number |  |
| `content[].smsId` | string |  |
| `content[].status` | object |  |
| `content[].status.date` | string |  |
| `content[].status.reason` | object |  |
| `content[].status.reason.description` | string |  |
| `content[].status.reason.detailedStatus` | string |  |
| `content[].status.status` | string |  |
| `content[].to` | string |  |
| `first` | boolean |  |
| `last` | boolean |  |
| `number` | number |  |
| `numberOfElements` | number |  |
| `size` | number |  |
| `totalElements` | number |  |
| `totalPages` | number |  |

## Native endpoint

Through the native Routee API, this operation is `POST /sms/tracking` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/track-multiple-messages-with-filters-for-a-specific-time-range.md) for the provider-specific parameters and requirements.

