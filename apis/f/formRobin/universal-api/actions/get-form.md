# FormRobin: Get Form

Retrieves a form from FormRobin.

```
GET https://connect.mindcloud.co/v1/universal/formRobin/latest/actions/get-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FormRobin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formRobin/latest/actions/get-form?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formRobin/latest/actions/get-form?${params}`, {
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
| `id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "emailNotificationsEnabled": true,
      "folderId": 1,
      "id": 1,
      "name": "Ava Chen",
      "redirectUrl": "https://example.com",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "webhookUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `emailNotificationsEnabled` | boolean |  |
| `folderId` | number |  |
| `id` | number |  |
| `name` | string |  |
| `redirectUrl` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |
| `webhookUrl` | string |  |

## Native endpoint

Through the native FormRobin API, this operation is `GET /forms/{{id}}` (base URL `https://formrobin.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form.md) for the provider-specific parameters and requirements.

