# Dialpad: List Contacts

Retrieves shared or local contacts from Dialpad.

```
GET https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dialpad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/list-contacts?${params}`, {
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
| `cursor` | string | no | A token used to return the next page of a previous request. Use the cursor provided in the previous response. |
| `include_local` | boolean | no | If set to true company local contacts will be included. |
| `owner_id` | string | no | The id of the user who owns the contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "displayName": "Ava Chen",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "ownerId": "string",
      "primaryEmail": "ava@example.com",
      "primaryPhone": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayName` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `ownerId` | string |  |
| `primaryEmail` | string |  |
| `primaryPhone` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Dialpad API, this operation is `GET /contacts` (base URL `https://dialpad.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

