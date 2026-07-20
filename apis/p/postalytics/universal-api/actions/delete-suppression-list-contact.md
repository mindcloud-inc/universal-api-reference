# Postalytics: Delete Suppression List Contact

Deletes a contact from a Postalytics suppression list.

```
DELETE https://connect.mindcloud.co/v1/universal/postalytics/latest/actions/delete-suppression-list-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postalytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/postalytics/latest/actions/delete-suppression-list-contact?connectionId=$CONNECTION_ID&listId=1&contactId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "1",
  "contactId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postalytics/latest/actions/delete-suppression-list-contact?${params}`, {
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
| `listId` | number | yes | Suppression list ID. |
| `contactId` | number | yes | Suppression contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider confirmation message. |

## Native endpoint

Through the native Postalytics API, this operation is `DELETE /api/v1/lists/suppression/contacts/:listId/:contactId` (base URL `https://api.postalytics.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-suppression-list-contact.md) for the provider-specific parameters and requirements.

