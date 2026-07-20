# Keap: Get Contact



```
GET https://connect.mindcloud.co/v1/universal/keap/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Keap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keap/latest/actions/get-contact?connectionId=$CONNECTION_ID&contact_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contact_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keap/latest/actions/get-contact?${params}`, {
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
| `contact_id` | string | yes | The unique identifier of the contact. |
| `fields` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "familyName": "Ava Chen",
      "givenName": "Ava Chen",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `familyName` | string |  |
| `givenName` | string |  |
| `id` | string |  |

## Native endpoint

Through the native Keap API, this operation is `GET /contacts/:contact_id` (base URL `https://api.infusionsoft.com/crm/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

