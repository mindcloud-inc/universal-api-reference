# Sakari SMS: Delete Contact

Deletes an existing contact from Sakari SMS.

```
DELETE https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/delete-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sakari SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/delete-contact?connectionId=$CONNECTION_ID&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/delete-contact?${params}`, {
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
| `contactId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Sakari SMS API, this operation is `DELETE /v1/accounts/:accountId/contacts/:contactId` (base URL `https://api.sakari.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact.md) for the provider-specific parameters and requirements.

