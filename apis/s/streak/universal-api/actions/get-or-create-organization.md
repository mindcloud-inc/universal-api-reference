# Streak: Get or Create Organization

Finds an organization in Streak, or creates one if needed.

```
POST https://connect.mindcloud.co/v1/universal/streak/latest/actions/get-or-create-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streak `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/streak/latest/actions/get-or-create-organization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamKey": "string",
  "domains[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/streak/latest/actions/get-or-create-organization', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamKey": "string",
    "domains[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamKey` | string | yes |  |
| `domains[]` | array<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        "string"
      ],
      "contactLinks": [
        {}
      ],
      "creationDate": "2026-05-07T12:00:00.000Z",
      "creatorKey": "string",
      "domains": [
        "string"
      ],
      "employeeCount": "string",
      "fields": {},
      "key": "string",
      "lastEnrichmentTimestamp": "2026-05-07T12:00:00.000Z",
      "lastSavedTimestamp": "2026-05-07T12:00:00.000Z",
      "lastSavedUserKey": "string",
      "name": "Ava Chen",
      "normalizedDomains": [
        "string"
      ],
      "orgLinks": [
        {}
      ],
      "other": "string",
      "phoneNumbers": [
        "string"
      ],
      "teamKey": "string",
      "versionTimestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses` | array<string> | Organization addresses. |
| `contactLinks` | array<object> | Linked contacts. |
| `creationDate` | date | When the organization was created. |
| `creatorKey` | string | The user who created the organization. |
| `domains` | array<string> | Domains associated with the organization. |
| `employeeCount` | string | Reported employee count range. |
| `fields` | object | Custom field values. |
| `key` | string | The organization key. |
| `lastEnrichmentTimestamp` | date | When the organization was last enriched. |
| `lastSavedTimestamp` | date | When the organization was last saved. |
| `lastSavedUserKey` | string | The user who last saved the organization. |
| `name` | string | The organization name. |
| `normalizedDomains` | array<string> | Normalized organization domains. |
| `orgLinks` | array<object> | Linked organizations. |
| `other` | string | Additional notes on the organization. |
| `phoneNumbers` | array<string> | Organization phone numbers. |
| `teamKey` | string | The team that owns the organization. |
| `versionTimestamp` | date | The current organization version timestamp. |

## Native endpoint

Through the native Streak API, this operation is `POST /api/v2/teams/:teamKey/organizations` (base URL `https://api.streak.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-or-create-organization.md) for the provider-specific parameters and requirements.

