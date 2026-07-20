# AvoSMS: Get Contact List

Retrieves a contact list and its contacts from AvoSMS.

```
GET https://connect.mindcloud.co/v1/universal/avoSMS/latest/actions/get-contact-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AvoSMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avoSMS/latest/actions/get-contact-list?connectionId=$CONNECTION_ID&listContactId=69cc2daf52244" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listContactId": "69cc2daf52244"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avoSMS/latest/actions/get-contact-list?${params}`, {
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
| `listContactId` | string | yes | Contact list ID Example: `69cc2daf52244`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AvoSMS API returns.

## Native endpoint

Through the native AvoSMS API, this operation is `POST /v1/contact/list/information` (base URL `https://api.avosms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-list.md) for the provider-specific parameters and requirements.

