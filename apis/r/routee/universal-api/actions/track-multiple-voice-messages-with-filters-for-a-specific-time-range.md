# Routee: Track multiple voice messages with filters for a specific time range

Tracks multiple voice messages with filters for a specific time range in Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/track-multiple-voice-messages-with-filters-for-a-specific-time-range
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/track-multiple-voice-messages-with-filters-for-a-specific-time-range?connectionId=$CONNECTION_ID&fieldName=Ava%20Chen&searchTerm=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fieldName": "Ava Chen",
  "searchTerm": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/track-multiple-voice-messages-with-filters-for-a-specific-time-range?${params}`, {
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
| `from` | string | no | ISO-8601 date-time format |
| `to` | string | no | ISO-8601 date-time format |
| `page` | number | no | The page number to retrieve, default value is 0 (meaning the first page) |
| `size` | number | no | The number of items to retrieve, default value is 20. |
| `sort` | string | no | The field name that will be used to sort the results. |
| `trackingId` | string | no | If provided then only the voice messages of the campaign with this tracking Id will be retrieved. |
| `tagged` | boolean | no |  |
| `fieldName` | string | yes | Defines the name of the field for this filter. ACCEPTED VALUES: id, recipient, from, collectedTones, groups, country, status.status, campaign |
| `searchOperator` | string | no | Defines the search operator to be used for the search. Examples: is, is_not, contains, starts_with, ends_with |
| `searchTerm` | string | yes | Defines the value of the specified field. |

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
| `content[].chargeInterval` | number |  |
| `content[].country` | string |  |
| `content[].direction` | string |  |
| `content[].duration` | number |  |
| `content[].from` | string |  |
| `content[].message` | object |  |
| `content[].message.gender` | string |  |
| `content[].message.language` | string |  |
| `content[].message.text` | string |  |
| `content[].messageId` | string |  |
| `content[].originatingService` | string |  |
| `content[].price` | number |  |
| `content[].recordings[]` | array |  |
| `content[].status` | object |  |
| `content[].status.date` | string |  |
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

Through the native Routee API, this operation is `POST /voice/tracking` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/track-multiple-voice-messages-with-filters-for-a-specific-time-range.md) for the provider-specific parameters and requirements.

