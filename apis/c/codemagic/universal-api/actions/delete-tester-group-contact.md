# Codemagic: Delete Tester Group Contact

Deletes a contact from a Codemagic tester group.

```
DELETE https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/delete-tester-group-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codemagic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/delete-tester-group-contact?connectionId=$CONNECTION_ID&contactId=string&testerGroupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "string",
  "testerGroupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/delete-tester-group-contact?${params}`, {
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
| `contactId` | string | yes | Tester group contact identifier. |
| `testerGroupId` | string | yes | Codemagic tester group identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Codemagic API returns.

## Native endpoint

Through the native Codemagic API, this operation is `DELETE /api/v3/tester-groups/:tester_group_id/contacts/:contact_id` (base URL `https://codemagic.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-tester-group-contact.md) for the provider-specific parameters and requirements.

