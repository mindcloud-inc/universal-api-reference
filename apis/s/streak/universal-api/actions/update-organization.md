# Streak: Update Organization

Updates an existing organization in Streak.

```
PUT https://connect.mindcloud.co/v1/universal/streak/latest/actions/update-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streak `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/streak/latest/actions/update-organization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/streak/latest/actions/update-organization', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationKey` | string | yes |  |
| `name` | string | no |  |
| `domains` | string | no |  |
| `industry` | string | no |  |
| `phoneNumbers` | string | no |  |
| `addresses` | string | no |  |
| `employeeCount` | string | no |  |
| `logoURL` | string | no |  |
| `other` | string | no |  |
| `twitterHandle` | string | no |  |
| `facebookHandle` | string | no |  |
| `linkedinHandle` | string | no |  |

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

Through the native Streak API, this operation is `POST /api/v2/organizations/:organizationKey` (base URL `https://api.streak.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-organization.md) for the provider-specific parameters and requirements.

