# Moosend: Get Subscriber By Email Address

Finds a subscriber in Moosend by email address.

```
GET https://connect.mindcloud.co/v1/universal/moosend/latest/actions/get-subscriber-by-email-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moosend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moosend/latest/actions/get-subscriber-by-email-address?connectionId=$CONNECTION_ID&mailingListId=string&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mailingListId": "string",
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moosend/latest/actions/get-subscriber-by-email-address?${params}`, {
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
| `mailingListId` | string | yes | The ID of the email list that contains the subscriber. |
| `email` | string | yes | The email address of the subscriber. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdOn": "2026-05-07T12:00:00.000Z",
      "customFields": [
        {}
      ],
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "preferences": [
        "string"
      ],
      "removedOn": "string",
      "subscribeMethod": 1,
      "subscribeType": 1,
      "tags": [
        "string"
      ],
      "unsubscribedFromID": "string",
      "unsubscribedOn": "string",
      "updatedOn": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdOn` | date |  |
| `customFields` | array<object> |  |
| `email` | string |  |
| `id` | string |  |
| `name` | string |  |
| `preferences` | array<string> |  |
| `removedOn` | string |  |
| `subscribeMethod` | number |  |
| `subscribeType` | number |  |
| `tags` | array<string> |  |
| `unsubscribedFromID` | string |  |
| `unsubscribedOn` | string |  |
| `updatedOn` | date |  |

## Native endpoint

Through the native Moosend API, this operation is `GET /subscribers/{{MailingListID}}/view.json` (base URL `https://api.moosend.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscriber-by-email-address.md) for the provider-specific parameters and requirements.

