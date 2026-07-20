# Conexteo: Get Contact List

Retrieves a contact list from Conexteo.

```
GET https://connect.mindcloud.co/v1/universal/conexteo/latest/actions/get-contact-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conexteo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/conexteo/latest/actions/get-contact-list?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/conexteo/latest/actions/get-contact-list?${params}`, {
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
| `id` | number | yes | Identifier of the contact list to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contacts_count": 1,
      "id": 1,
      "name": "Ava Chen",
      "rcsCapabilityStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contacts_count` | number | Number of contacts in the list. |
| `id` | number | Contact-list identifier. |
| `name` | string | Contact-list name. |
| `rcsCapabilityStatus` | string | Provider RCS capability status for the list. |

## Native endpoint

Through the native Conexteo API, this operation is `GET /contactlists/:id` (base URL `https://api.conexteo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-list.md) for the provider-specific parameters and requirements.

