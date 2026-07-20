# Moosend: Add Multiple Subscribers

Creates multiple subscribers in Moosend.

```
POST https://connect.mindcloud.co/v1/universal/moosend/latest/actions/add-multiple-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moosend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moosend/latest/actions/add-multiple-subscribers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mailingListId": "string",
  "subscribers": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moosend/latest/actions/add-multiple-subscribers', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mailingListId": "string",
    "subscribers": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mailingListId` | string | yes | The ID of the email list where you want to add multiple subscribers. |
| `hasExternalDoubleOptIn` | boolean | no | When true , it flags the added subscribers as having given their subscription consent by other means. |
| `subscribers` | list<object> | yes | A list containing up to 1000 subscribers that you are adding to the email list. You must specify the Name , Email , and CustomFields for each subscriber. |
| `tags` | object | no | The member tag you can use to filter members by when working with an email list. |
| `preferences` | object | no | The member preferences you can user to segment or filter members by, when working with an email list. |

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
| `removedOn` | string |  |
| `subscribeMethod` | number |  |
| `subscribeType` | number |  |
| `tags` | array<string> |  |
| `unsubscribedFromID` | string |  |
| `unsubscribedOn` | string |  |
| `updatedOn` | date |  |

## Native endpoint

Through the native Moosend API, this operation is `POST /subscribers/{{MailingListID}}/subscribe-many.json` (base URL `https://api.moosend.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-multiple-subscribers.md) for the provider-specific parameters and requirements.

