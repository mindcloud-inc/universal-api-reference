# Nimble: List Contact Notes

Retrieves notes for a contact from Nimble.

```
GET https://connect.mindcloud.co/v1/universal/nimble/latest/actions/list-contact-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nimble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nimble/latest/actions/list-contact-notes?connectionId=$CONNECTION_ID&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nimble/latest/actions/list-contact-notes?${params}`, {
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
| `contactId` | string | yes | Nimble contact_id path parameter. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Nimble API returns.

## Native endpoint

Through the native Nimble API, this operation is `GET /api/v1/contact/:contact_id/notes` (base URL `https://app.nimble.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-notes.md) for the provider-specific parameters and requirements.

