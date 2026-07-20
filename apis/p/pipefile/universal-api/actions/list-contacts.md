# Pipefile: List Contacts

Finds contacts in Pipefile by optional filters.

```
GET https://connect.mindcloud.co/v1/universal/pipefile/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipefile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipefile/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipefile/latest/actions/list-contacts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "emailBounced": true,
      "emailComplained": true,
      "name": "Ava Chen",
      "phone": "string",
      "phoneUnreachable": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Primary email address for the contact. |
| `emailBounced` | boolean | Whether Pipefile marks the contact email as bounced. |
| `emailComplained` | boolean | Whether Pipefile marks the contact email as complained. |
| `name` | string | Contact name returned by Pipefile. |
| `phone` | string | Primary phone number for the contact. |
| `phoneUnreachable` | boolean | Whether Pipefile marks the contact phone as unreachable. |

## Native endpoint

Through the native Pipefile API, this operation is `GET /contacts/` (base URL `https://api.pipefile.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

