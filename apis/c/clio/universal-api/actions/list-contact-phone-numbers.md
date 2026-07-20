# Clio Manage: List Contact Phone Numbers

Retrieves phone numbers for a contact in Clio Manage.

```
GET https://connect.mindcloud.co/v1/universal/clio/latest/actions/list-contact-phone-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clio Manage `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clio/latest/actions/list-contact-phone-numbers?connectionId=$CONNECTION_ID&limit=25&offset=0&contactId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "contactId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clio/latest/actions/list-contact-phone-numbers?${params}`, {
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
| `contactId` | number | yes | The Clio contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "etag": "string",
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `etag` | string |  |
| `id` | number |  |

## Native endpoint

Through the native Clio Manage API, this operation is `GET /contacts/:contact_id/phone_numbers.json` (base URL `https://app.clio.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contact-phone-numbers.md) for the provider-specific parameters and requirements.

