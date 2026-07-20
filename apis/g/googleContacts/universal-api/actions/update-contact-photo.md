# Google Contacts: Update Contact Photo

Updates a contact photo in Google Contacts.

```
PUT https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/update-contact-photo
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Contacts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/update-contact-photo" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "resourceName": "Ava Chen",
  "photoBytes": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/update-contact-photo', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "resourceName": "Ava Chen",
    "photoBytes": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `resourceName` | string | yes |  |
| `photoBytes` | string | yes | Base64-encoded photo bytes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "resourceName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `resourceName` | string |  |

## Native endpoint

Through the native Google Contacts API, this operation is `PATCH /v1/people/:resourceName:photoAction` (base URL `https://people.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact-photo.md) for the provider-specific parameters and requirements.

