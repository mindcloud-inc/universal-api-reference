# MojoTxt: List Subscription Lists

Retrieves subscription lists from MojoTxt.

```
GET https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/list-subscription-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MojoTxt `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/list-subscription-lists?connectionId=$CONNECTION_ID&limit=25&offset=0&phoneNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "phoneNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/list-subscription-lists?${params}`, {
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
| `phoneNumber` | string | yes | The MojoTxt phone number in international format, like +17792533748. |
| `stats` | string | no | Set to 1 to include subscription list statistics in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Keyword": "string",
      "ListID": 1,
      "ListName": "Ava Chen",
      "SendLastMessage": 1,
      "SubscriberCount": 1,
      "WelcomeMessage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Keyword` | string | The unique keyword for the subscription list. |
| `ListID` | number | The unique identifier for the subscription list. |
| `ListName` | string | The descriptive name of the subscription list. |
| `SendLastMessage` | number | Whether the last sent message should be sent to new subscribers. |
| `SubscriberCount` | number | The number of subscribers in the list. |
| `WelcomeMessage` | string | The welcome message sent when a person joins the list. |

## Native endpoint

Through the native MojoTxt API, this operation is `GET /:phoneNumber/lists/list` (base URL `https://app.mojotxt.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-subscription-lists.md) for the provider-specific parameters and requirements.

