# Ubidots: Get Organization



```
GET https://connect.mindcloud.co/v1/universal/ubidots/latest/actions/get-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ubidots `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ubidots/latest/actions/get-organization?connectionId=$CONNECTION_ID&organizationKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ubidots/latest/actions/get-organization?${params}`, {
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
| `organizationKey` | string | yes | The organization ID or key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "app": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dashboardsUrl": "https://example.com",
      "description": "string",
      "devicesUrl": "https://example.com",
      "id": "string",
      "isActive": true,
      "label": "string",
      "logo": "string",
      "name": "Ava Chen",
      "properties": {},
      "tags": [
        "string"
      ],
      "url": "https://example.com",
      "usersUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `app` | object |  |
| `createdAt` | date |  |
| `dashboardsUrl` | string |  |
| `description` | string |  |
| `devicesUrl` | string |  |
| `id` | string |  |
| `isActive` | boolean |  |
| `label` | string |  |
| `logo` | string |  |
| `name` | string |  |
| `properties` | object |  |
| `tags` | array<string> |  |
| `url` | string |  |
| `usersUrl` | string |  |

## Native endpoint

Through the native Ubidots API, this operation is `GET /organizations/:organization_key/` (base URL `https://industrial.api.ubidots.com/api/v2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization.md) for the provider-specific parameters and requirements.

