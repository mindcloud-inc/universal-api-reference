# Magileads: Get Contact

Retrieves a contact profile from a Magileads contact list.

```
GET https://connect.mindcloud.co/v1/universal/magileads/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Magileads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/magileads/latest/actions/get-contact?connectionId=$CONNECTION_ID&contact_list_id=1&contact_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contact_list_id": "1",
  "contact_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/magileads/latest/actions/get-contact?${params}`, {
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
| `contact_list_id` | number | yes | The contact list ID. |
| `contact_id` | number | yes | The contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact_profile": {},
      "state": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact_profile` | object |  |
| `state` | boolean |  |

## Native endpoint

Through the native Magileads API, this operation is `GET /contact-lists/:contact_list_id/contacts/:contact_id` (base URL `https://app.api-magileads.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

