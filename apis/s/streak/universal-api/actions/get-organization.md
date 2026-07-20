# Streak: Get Organization

Retrieves an organization from Streak.

```
GET https://connect.mindcloud.co/v1/universal/streak/latest/actions/get-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streak `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/streak/latest/actions/get-organization?connectionId=$CONNECTION_ID&organizationKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/streak/latest/actions/get-organization?${params}`, {
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
| `organizationKey` | string | yes | Organization key. |

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
| `addresses` | array<string> | The organization addresses. |
| `contactLinks` | array<object> | Links from this organization to related contacts. |
| `creationDate` | date | When the organization was created. |
| `creatorKey` | string | The user who created the organization. |
| `domains` | array<string> | The organization domains. |
| `employeeCount` | string | The organization employee count range. |
| `fields` | object | Custom field values keyed by field ID. |
| `key` | string | The organization key. |
| `lastEnrichmentTimestamp` | date | When the organization was last enriched. |
| `lastSavedTimestamp` | date | When the organization was last saved. |
| `lastSavedUserKey` | string | The user who last saved the organization. |
| `name` | string | The organization name. |
| `normalizedDomains` | array<string> | Normalized organization domains. |
| `orgLinks` | array<object> | Links from this organization to related organizations. |
| `phoneNumbers` | array<string> | The organization phone numbers. |
| `teamKey` | string | The team the organization belongs to. |
| `versionTimestamp` | date | When the current organization version was written. |

## Native endpoint

Through the native Streak API, this operation is `GET /api/v2/organizations/:organizationKey` (base URL `https://api.streak.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization.md) for the provider-specific parameters and requirements.

