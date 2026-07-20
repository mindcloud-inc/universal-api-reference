# FormRobin: Update Form

Updates an existing form in FormRobin.

```
PUT https://connect.mindcloud.co/v1/universal/formRobin/latest/actions/update-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FormRobin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/formRobin/latest/actions/update-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formRobin/latest/actions/update-form', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The FormRobin form ID to update. |
| `name` | string | no | The form name. Example: `MindCloud Wizard Test Form Updated`. |
| `emailNotificationsEnabled` | boolean | no | Whether email notifications are enabled for the form. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `folderId` | number | no | The destination folder ID for the form. |
| `data` | object | no | Form configuration data. |
| `redirectUrl` | string | no | The URL to redirect to after form submission. |
| `webhookUrl` | string | no | The webhook URL that receives form submissions. |

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

Through the native FormRobin API, this operation is `PUT /forms/{{id}}` (base URL `https://formrobin.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-form.md) for the provider-specific parameters and requirements.

