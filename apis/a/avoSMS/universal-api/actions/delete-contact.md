# AvoSMS: Delete Contact

Deletes an existing contact from AvoSMS.

```
DELETE https://connect.mindcloud.co/v1/universal/avoSMS/latest/actions/delete-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AvoSMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/avoSMS/latest/actions/delete-contact?connectionId=$CONNECTION_ID&listContactId=69cc2daf52244&contactTelephoneNumber=33612345678" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listContactId": "69cc2daf52244",
  "contactTelephoneNumber": "33612345678"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avoSMS/latest/actions/delete-contact?${params}`, {
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
| `contactTelephoneNumber` | string | yes | Phone number of the contact to delete Example: `33612345678`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AvoSMS API returns.

## Native endpoint

Through the native AvoSMS API, this operation is `POST /v1/contact/delete` (base URL `https://api.avosms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact.md) for the provider-specific parameters and requirements.

