# Karma CRM: Get Company

Retrieves a specific company from Karma CRM.

```
GET https://connect.mindcloud.co/v1/universal/karmaCRM/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Karma CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/karmaCRM/latest/actions/get-company?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/karmaCRM/latest/actions/get-company?${params}`, {
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
| `id` | number | yes | The ID of the company to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatarUrl": "https://example.com",
      "background": "string",
      "createdAt": "string",
      "createdById": 1,
      "id": 1,
      "name": "Ava Chen",
      "organizationId": 1,
      "private": true,
      "updatedAt": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarUrl` | string |  |
| `background` | string |  |
| `createdAt` | string |  |
| `createdById` | number |  |
| `id` | number |  |
| `name` | string |  |
| `organizationId` | number |  |
| `private` | boolean |  |
| `updatedAt` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native Karma CRM API, this operation is `GET /api/v3/companies/:id.json` (base URL `https://app.karmacrm.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.

