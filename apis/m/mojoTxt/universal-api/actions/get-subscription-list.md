# MojoTxt: Get Subscription List

Retrieves a subscription list from MojoTxt.

```
GET https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/get-subscription-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MojoTxt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/get-subscription-list?connectionId=$CONNECTION_ID&listIdOrKeyword=string&phoneNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listIdOrKeyword": "string",
  "phoneNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/get-subscription-list?${params}`, {
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
| `listIdOrKeyword` | string | yes | The subscription list identifier or keyword value to retrieve. |
| `phoneNumber` | string | yes | The MojoTxt phone number in international format, like +17792533748. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AutomationCount": 1,
      "Keyword": "string",
      "KeywordID": 1,
      "Listed": 1,
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
| `AutomationCount` | number | The number of automations configured for the list. |
| `Keyword` | string | The unique keyword for the subscription list. |
| `KeywordID` | number | The keyword identifier associated with the subscription list. |
| `Listed` | number | Whether the list is active and listed. |
| `ListID` | number | The unique identifier for the subscription list. |
| `ListName` | string | The descriptive name of the subscription list. |
| `SendLastMessage` | number | Whether the last sent message should be sent to new subscribers. |
| `SubscriberCount` | number | The number of subscribers in the list. |
| `WelcomeMessage` | string | The welcome message sent when a person joins the list. |

## Native endpoint

Through the native MojoTxt API, this operation is `GET /:phoneNumber/lists/get/:listIdOrKeyword` (base URL `https://app.mojotxt.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscription-list.md) for the provider-specific parameters and requirements.

