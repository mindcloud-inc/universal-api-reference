# Webex Interact: Delete contact

Deletes an existing contact from Webex Interact.

```
DELETE https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/delete-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webex Interact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/delete-contact?connectionId=$CONNECTION_ID&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/delete-contact?${params}`, {
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
| `contactId` | string | yes | Contact ID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactId": "string",
      "status_code": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactId` | string |  |
| `status_code` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native Webex Interact API, this operation is `DELETE /contacts/v1/contacts/{contactId}` (base URL `https://api.webexinteract.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact.md) for the provider-specific parameters and requirements.

