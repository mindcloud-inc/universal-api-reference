# Maildroppa: List Filtered Subscribers

Finds Maildroppa subscribers by segment expression.

```
GET https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/list-filtered-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildroppa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/list-filtered-subscribers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/list-filtered-subscribers?${params}`, {
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
| `filterGroups[]` | array | no | Filter groups that compose this expression. |
| `operator` | string | no | Logical operator that applies between filter groups. |
| `pageNumber` | number | no | Page number. |
| `pageSize` | number | no | Number of items per page. |
| `status` | string | no | Subscriber status filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "gdprAgreement": "string",
          "id": "string",
          "registeredAt": "string",
          "subscriberStatus": "string",
          "tags": [
            "string"
          ],
          "values": [
            {}
          ]
        }
      ],
      "pageNumber": 1,
      "pageSize": 1,
      "totalItems": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[].gdprAgreement` | string | Text of GDPR agreement if applicable. |
| `items[].id` | string | Unique identifier of the subscriber. |
| `items[].registeredAt` | string | Registration date/time of the subscriber. |
| `items[].subscriberStatus` | string | Subscriber's status. |
| `items[].tags` | array<string> | List of tag identifiers associated with the subscriber. |
| `items[].values` | array<object> | List of custom fields for the subscriber. |
| `pageNumber` | number | Which page is this (1-based index)? |
| `pageSize` | number | Number of items per page. |
| `totalItems` | number | Total number of items matching the query. |
| `totalPages` | number | Total number of pages based on page size. |

## Native endpoint

Through the native Maildroppa API, this operation is `POST /subscribers/filtered` (base URL `https://api.maildroppa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-filtered-subscribers.md) for the provider-specific parameters and requirements.

