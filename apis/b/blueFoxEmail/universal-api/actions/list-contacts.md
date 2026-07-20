# BlueFox Email: List Contacts

Retrieves contacts from BlueFox Email.

```
GET https://connect.mindcloud.co/v1/universal/blueFoxEmail/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlueFox Email `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blueFoxEmail/latest/actions/list-contacts?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blueFoxEmail/latest/actions/list-contacts?${params}`, {
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
| `projectId` | string | yes | BlueFox project ID from the target project settings. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "Id": "string",
      "Lists": [
        "string"
      ],
      "projectId": "string",
      "tags": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "V": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string | BlueFox account ID. |
| `createdAt` | date | When the contact was created. |
| `email` | string | Contact email address. |
| `Id` | string | BlueFox contact ID. |
| `Lists` | array<string> | Subscriber lists the contact belongs to. |
| `projectId` | string | BlueFox project ID. |
| `tags` | array<string> | Tags assigned to the contact. |
| `updatedAt` | date | When the contact was last updated. |
| `V` | number | BlueFox internal version number. |

## Native endpoint

Through the native BlueFox Email API, this operation is `GET /v1/contacts/:projectId` (base URL `https://api.bluefox.email`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

