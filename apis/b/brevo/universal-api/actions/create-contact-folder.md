# Brevo: Create Contact Folder



```
POST https://connect.mindcloud.co/v1/universal/brevo/latest/actions/create-contact-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brevo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/brevo/latest/actions/create-contact-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/brevo/latest/actions/create-contact-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The contact folder name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | The created folder id. |

## Native endpoint

Through the native Brevo API, this operation is `POST /v3/contacts/folders` (base URL `https://api.brevo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact-folder.md) for the provider-specific parameters and requirements.

