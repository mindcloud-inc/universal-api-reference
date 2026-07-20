# Routee: Track multiple Email Validator requests with filters based on specific time range

Tracks multiple email validator requests with filters based on specific time range in Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/track-multiple-email-validator-requests-with-filters-based-on-specific-time-range
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/track-multiple-email-validator-requests-with-filters-based-on-specific-time-range?connectionId=$CONNECTION_ID&dateStart=string&dateEnd=string&fieldName=Ava%20Chen&searchTerm=string&searchOperator=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dateStart": "string",
  "dateEnd": "string",
  "fieldName": "Ava Chen",
  "searchTerm": "string",
  "searchOperator": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/track-multiple-email-validator-requests-with-filters-based-on-specific-time-range?${params}`, {
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
| `dateStart` | string | yes | ISO-8601 date-time format. |
| `dateEnd` | string | yes | ISO-8601 date-time format. |
| `page` | string | no | The page number to retrieve, default value is 0 (meaning the first page). |
| `size` | string | no | The number of items to retrieve, default value is 20. Max value is 2000. |
| `fieldName` | string | yes | The name of the field to apply the filtering. Available values: email, exists, trackingId, hasValidFormat, hasValidDNS, label, |
| `searchTerm` | string | yes | The exact value that the specified field must match. |
| `searchOperator` | string | yes | The operator upon which the search operation will be executed. Possible values: 'IS', 'IS_NOT', 'CONTAINS', 'STARTS_WITH', 'ENDS_WITH'. |

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
| `content[].createdAt` | string |  |
| `content[].details` | object |  |
| `content[].details.exists` | boolean |  |
| `content[].details.hasValidDNS` | boolean |  |
| `content[].details.hasValidFormat` | boolean |  |
| `content[].email` | string |  |
| `content[].label` | string |  |
| `content[].price` | number |  |
| `content[].trackingId` | string |  |
| `first` | boolean |  |
| `last` | boolean |  |
| `number` | number |  |
| `numberOfElements` | number |  |
| `size` | number |  |
| `totalElements` | number |  |
| `totalPages` | number |  |

## Native endpoint

Through the native Routee API, this operation is `POST /emailvalidator/tracking` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/track-multiple-email-validator-requests-with-filters-based-on-specific-time-range.md) for the provider-specific parameters and requirements.

