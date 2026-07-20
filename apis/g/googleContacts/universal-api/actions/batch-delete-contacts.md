# Google Contacts: Batch Delete Contacts

Deletes multiple contacts from Google Contacts.

```
DELETE https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/batch-delete-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Contacts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/batch-delete-contacts?connectionId=$CONNECTION_ID&resourceNames%5B%5D=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resourceNames[]": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/batch-delete-contacts?${params}`, {
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
| `resourceNames[]` | array<string> | yes | Array of contact resource names to delete (e.g. people/c123). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "resourceNames": [
        "Ava Chen"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `resourceNames[]` | string |  |

## Native endpoint

Through the native Google Contacts API, this operation is `POST /v1/people\:batchDeleteContacts` (base URL `https://people.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-delete-contacts.md) for the provider-specific parameters and requirements.

