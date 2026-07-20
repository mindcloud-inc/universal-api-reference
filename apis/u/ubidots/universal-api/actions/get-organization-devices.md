# Ubidots: Get Organization Devices



```
GET https://connect.mindcloud.co/v1/universal/ubidots/latest/actions/get-organization-devices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ubidots `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ubidots/latest/actions/get-organization-devices?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizationKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ubidots/latest/actions/get-organization-devices?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "isActive": true,
      "label": "string",
      "name": "Ava Chen",
      "organization": {},
      "properties": {},
      "tags": [
        "string"
      ],
      "url": "https://example.com",
      "variables": "string",
      "variablesNumber": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `description` | string |  |
| `id` | string |  |
| `isActive` | boolean |  |
| `label` | string |  |
| `name` | string |  |
| `organization` | object |  |
| `properties` | object |  |
| `tags` | array<string> |  |
| `url` | string |  |
| `variables` | string |  |
| `variablesNumber` | number |  |

## Native endpoint

Through the native Ubidots API, this operation is `GET /organizations/:organization_key/devices/` (base URL `https://industrial.api.ubidots.com/api/v2.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-organization-devices.md) for the provider-specific parameters and requirements.

