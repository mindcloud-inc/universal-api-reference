# Notifyre SMS: Delete Groups

Deletes selected groups from Notifyre address book.

```
DELETE https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/delete-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notifyre SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/delete-groups?connectionId=$CONNECTION_ID&groups=string&includeContacts=true" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groups": "string",
  "includeContacts": "true"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/delete-groups?${params}`, {
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
| `groups` | list<string> | yes | Groups to delete. |
| `includeContacts` | boolean | yes | Whether contacts should also be removed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean | Whether the groups were deleted successfully. |

## Native endpoint

Through the native Notifyre SMS API, this operation is `DELETE /addressbook/groups` (base URL `https://api.notifyre.com/20220711`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-groups.md) for the provider-specific parameters and requirements.

