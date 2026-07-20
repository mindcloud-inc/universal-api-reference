# SuperSend: Remove Contact Profile Label

Deletes a profile label from a SuperSend contact.

```
DELETE https://connect.mindcloud.co/v1/universal/superSend/latest/actions/remove-contact-profile-label
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/remove-contact-profile-label?connectionId=$CONNECTION_ID&id=string&labelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "labelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superSend/latest/actions/remove-contact-profile-label?${params}`, {
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
| `id` | string | yes | Resource ID (UUID) |
| `labelId` | string | yes | Label UUID to remove from the contact's profile |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "request_id": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `request_id` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native SuperSend API, this operation is `DELETE /contacts/{id}/profile-labels/{labelId}` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-contact-profile-label.md) for the provider-specific parameters and requirements.

