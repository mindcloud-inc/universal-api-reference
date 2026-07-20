# BigMailer: Get Contact

Retrieves a contact from a BigMailer brand.

```
GET https://connect.mindcloud.co/v1/universal/bigMailer/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigMailer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigMailer/latest/actions/get-contact?connectionId=$CONNECTION_ID&brandId=string&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "brandId": "string",
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigMailer/latest/actions/get-contact?${params}`, {
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
| `brandId` | string | yes | ID of the brand containing the contact. |
| `contactId` | string | yes | ID or email address of the contact. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BigMailer API returns.

## Native endpoint

Through the native BigMailer API, this operation is `GET /brands/:brand_id/contacts/:contact_id` (base URL `https://api.bigmailer.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

