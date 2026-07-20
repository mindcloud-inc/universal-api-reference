# Webex Interact: Delete contact list

Deletes an existing contact list from Webex Interact.

```
DELETE https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/delete-contact-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webex Interact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/delete-contact-list?connectionId=$CONNECTION_ID&uid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/delete-contact-list?${params}`, {
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
| `uid` | string | yes | Contact list UID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status_code": 1,
      "success": true,
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status_code` | number |  |
| `success` | boolean |  |
| `uid` | string |  |

## Native endpoint

Through the native Webex Interact API, this operation is `DELETE /contacts/v1/lists/{uid}` (base URL `https://api.webexinteract.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact-list.md) for the provider-specific parameters and requirements.

