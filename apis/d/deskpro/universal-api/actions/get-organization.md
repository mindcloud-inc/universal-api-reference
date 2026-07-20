# Deskpro: Get Organization

Retrieves an organization record from Deskpro.

```
GET https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/get-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deskpro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/get-organization?connectionId=$CONNECTION_ID&organizationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/get-organization?${params}`, {
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
| `organizationId` | number | yes | Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chatsCount": 1,
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "emailDomains": [
        "ava@example.com"
      ],
      "id": 1,
      "importance": 1,
      "name": "Ava Chen",
      "parent": 1,
      "phoneNumbers": [
        "string"
      ],
      "summary": "string",
      "ticketsCount": 1,
      "userGroups": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chatsCount` | number |  |
| `dateCreated` | date |  |
| `emailDomains[]` | string |  |
| `id` | number |  |
| `importance` | number |  |
| `name` | string |  |
| `parent` | number |  |
| `phoneNumbers[]` | string |  |
| `summary` | string |  |
| `ticketsCount` | number |  |
| `userGroups[]` | number |  |

## Native endpoint

Through the native Deskpro API, this operation is `GET /organizations/:organizationId` (base URL `{{credentials.helpdeskUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization.md) for the provider-specific parameters and requirements.

