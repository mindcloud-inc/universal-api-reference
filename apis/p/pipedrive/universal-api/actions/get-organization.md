# Pipedrive: Get Organization

Retrieves an organization from Pipedrive.

```
GET https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/get-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/get-organization?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/get-organization?${params}`, {
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
| `id` | number | yes | Unique ID of the organization. |
| `includeFields` | string | no | Comma-separated additional fields to include. |
| `customFields` | string | no | Comma-separated custom field keys to include. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "addTime": "string",
      "annualRevenue": {},
      "customFields": {},
      "employeeCount": {},
      "id": 1,
      "industry": {},
      "isDeleted": true,
      "linkedin": {},
      "name": "Ava Chen",
      "ownerId": 1,
      "updateTime": "string",
      "visibleTo": 1,
      "website": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `addTime` | string |  |
| `annualRevenue` | object |  |
| `customFields` | object |  |
| `employeeCount` | object |  |
| `id` | number |  |
| `industry` | object |  |
| `isDeleted` | boolean |  |
| `linkedin` | object |  |
| `name` | string |  |
| `ownerId` | number |  |
| `updateTime` | string |  |
| `visibleTo` | number |  |
| `website` | object |  |

## Native endpoint

Through the native Pipedrive API, this operation is `GET v2/organizations/:id` (base URL `{{credentials.accessTokenRequest.api_domain}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization.md) for the provider-specific parameters and requirements.

