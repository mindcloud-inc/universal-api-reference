# EZ Texting: Delete Contact

Deletes a contact from EZ Texting.

```
DELETE https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/delete-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EZ Texting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/delete-contact?connectionId=$CONNECTION_ID&phoneNumber=(737)%20337-8315" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "phoneNumber": "(737) 337-8315"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/delete-contact?${params}`, {
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
| `phoneNumber` | string | yes | Phone number Example: `(737) 337-8315`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EZ Texting API returns.

## Native endpoint

Through the native EZ Texting API, this operation is `DELETE /contacts/:phoneNumber` (base URL `https://a.eztexting.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact.md) for the provider-specific parameters and requirements.

