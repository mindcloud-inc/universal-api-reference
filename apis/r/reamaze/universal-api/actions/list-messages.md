# Reamaze: List Messages



```
GET https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/list-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reamaze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/list-messages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/list-messages?${params}`, {
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
| `filter` | string | no | `filter` with `staff` will show only staff messages and `customer` will show only customer messages. |
| `staff` | string | no | `filter` with `staff` will show only staff messages and `customer` will show only customer messages. |
| `tag` | string | no | `tag` with string value (comma separated) will return messages belonging to conversations matching specific tags. |
| `origin` | string | no | `origin` with number value will return messages from a specific origin (see below note on origin values). |
| `sentBy` | string | no | `sent_by` with a value matching a known user `email` will return only messages sent by that user. |
| `email` | string | no | `sent_by` with a value matching a known user `email` will return only messages sent by that user. |
| `category` | string | no | `category` with a string value will return messages from a specific Channel (internally called `category`) matching the `slug` value. |
| `startDate` | date | no | `start_date` and `end_date` (ISO8601 format) will allow filtering of messages by creation date. |
| `endDate` | date | no | `start_date` and `end_date` (ISO8601 format) will allow filtering of messages by creation date. |
| `include` | string | no | `include` with the value `original_body` will return an additional `original_body` attribute that is the message's HTML, if present. |
| `originalBody` | string | no | `include` with the value `original_body` will return an additional `original_body` attribute that is the message's HTML, if present. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "messages": [
        {}
      ],
      "pageCount": 1,
      "pageSize": 1,
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `messages` | array<object> |  |
| `pageCount` | number |  |
| `pageSize` | number |  |
| `totalCount` | number |  |

## Native endpoint

Through the native Reamaze API, this operation is `GET /messages` (base URL `https://{{credentials.brand}}.reamaze.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-messages.md) for the provider-specific parameters and requirements.

