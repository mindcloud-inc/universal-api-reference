# AvoSMS: Create Contact List

Creates a new contact list in AvoSMS.

```
POST https://connect.mindcloud.co/v1/universal/avoSMS/latest/actions/create-contact-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AvoSMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/avoSMS/latest/actions/create-contact-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listContactName": "MindCloud FR",
  "listContactCountryCode": "FR"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/avoSMS/latest/actions/create-contact-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listContactName": "MindCloud FR",
    "listContactCountryCode": "FR"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listContactName` | string | yes | Name of the contact list Example: `MindCloud FR`. |
| `listContactCountryCode` | string | yes | ISO2 country code of the contact list Example: `FR`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AvoSMS API returns.

## Native endpoint

Through the native AvoSMS API, this operation is `POST /v1/contact/list/create` (base URL `https://api.avosms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact-list.md) for the provider-specific parameters and requirements.

