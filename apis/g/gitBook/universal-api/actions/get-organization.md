# GitBook: Get Organization

Retrieves organization details from GitBook by ID.

```
GET https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/get-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/get-organization?connectionId=$CONNECTION_ID&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/get-organization?${params}`, {
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
| `organizationId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "defaultRole": "string",
      "emailDomains": [
        "ava@example.com"
      ],
      "id": "string",
      "inviteLinks": true,
      "plan": "string",
      "title": "string",
      "type": "string",
      "urls": {
        "app": "https://example.com",
        "location": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `defaultRole` | string |  |
| `emailDomains` | array<string> |  |
| `id` | string |  |
| `inviteLinks` | boolean |  |
| `plan` | string |  |
| `title` | string |  |
| `type` | string |  |
| `urls.app` | string |  |
| `urls.location` | string |  |

## Native endpoint

Through the native GitBook API, this operation is `GET /orgs/:organizationId` (base URL `https://api.gitbook.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization.md) for the provider-specific parameters and requirements.

