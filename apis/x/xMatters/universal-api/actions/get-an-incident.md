# xMatters: Get an incident

Retrieves an incident from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-an-incident
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-an-incident?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-an-incident?${params}`, {
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
| `incidentId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commander": {
        "firstName": "Ava",
        "id": "string",
        "lastName": "Chen",
        "licenseType": "string",
        "links": {
          "self": "https://example.com"
        },
        "recipientType": "string",
        "targetName": "Ava Chen"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "incidentIdentifier": "string",
      "initiatedBy": {
        "firstName": "Ava",
        "id": "string",
        "lastName": "Chen",
        "licenseType": "string",
        "links": {
          "self": "https://example.com"
        },
        "recipientType": "string",
        "targetName": "Ava Chen"
      },
      "links": {
        "self": "https://example.com"
      },
      "severity": {
        "name": "Ava Chen"
      },
      "status": {
        "name": "Ava Chen"
      },
      "summary": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commander.firstName` | string |  |
| `commander.id` | string |  |
| `commander.lastName` | string |  |
| `commander.licenseType` | string |  |
| `commander.links.self` | string |  |
| `commander.recipientType` | string |  |
| `commander.targetName` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `id` | string |  |
| `incidentIdentifier` | string |  |
| `initiatedBy.firstName` | string |  |
| `initiatedBy.id` | string |  |
| `initiatedBy.lastName` | string |  |
| `initiatedBy.licenseType` | string |  |
| `initiatedBy.links.self` | string |  |
| `initiatedBy.recipientType` | string |  |
| `initiatedBy.targetName` | string |  |
| `links.self` | string |  |
| `severity.name` | string |  |
| `status.name` | string |  |
| `summary` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native xMatters API, this operation is `GET incidents/{incidentId}` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-an-incident.md) for the provider-specific parameters and requirements.

