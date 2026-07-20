# BlueFox Email: Delete Contact

Deletes a contact from BlueFox Email.

```
DELETE https://connect.mindcloud.co/v1/universal/blueFoxEmail/latest/actions/delete-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlueFox Email `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/blueFoxEmail/latest/actions/delete-contact?connectionId=$CONNECTION_ID&projectId=string&contactEmailAddress=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "contactEmailAddress": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blueFoxEmail/latest/actions/delete-contact?${params}`, {
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
| `projectId` | string | yes | BlueFox project ID. |
| `contactEmailAddress` | string | yes | Email address of the contact to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "__v": 1,
      "_id": "string",
      "accountId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "lastReceiveDate": "2026-05-07T12:00:00.000Z",
      "projectId": "string",
      "tags": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `__v` | number |  |
| `_id` | string |  |
| `accountId` | string |  |
| `createdAt` | date |  |
| `email` | string |  |
| `lastReceiveDate` | date |  |
| `projectId` | string |  |
| `tags` | array<string> |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native BlueFox Email API, this operation is `DELETE /v1/contacts/:projectId/:contactEmailAddress` (base URL `https://api.bluefox.email`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact.md) for the provider-specific parameters and requirements.

