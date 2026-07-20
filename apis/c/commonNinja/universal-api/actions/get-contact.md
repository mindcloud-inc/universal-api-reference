# Common Ninja: Get Contact

Retrieves a project contact from Common Ninja.

```
GET https://connect.mindcloud.co/v1/universal/commonNinja/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Common Ninja `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/commonNinja/latest/actions/get-contact?connectionId=$CONNECTION_ID&projectId=string&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/commonNinja/latest/actions/get-contact?${params}`, {
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
| `projectId` | string | yes | The project ID. |
| `contactId` | string | yes | The contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "company": "string",
      "contactId": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "name": "Ava Chen",
      "notes": [
        "string"
      ],
      "phone": "string",
      "projectId": "string",
      "source": "string",
      "thumbnail": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `company` | string |  |
| `contactId` | string |  |
| `created` | date |  |
| `email` | string |  |
| `name` | string |  |
| `notes` | array<string> |  |
| `phone` | string |  |
| `projectId` | string |  |
| `source` | string |  |
| `thumbnail` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native Common Ninja API, this operation is `GET /projects/:projectId/contacts/:contactId` (base URL `https://api.commoninja.com/platform/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

