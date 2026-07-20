# xMatters: Delete a temporary absence

Deletes a temporary absence from your xMatters instance.

```
DELETE https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/delete-a-temporary-absence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/delete-a-temporary-absence?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/delete-a-temporary-absence?${params}`, {
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
| `temporaryAbsenceId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "absenceType": "string",
      "end": "2026-05-07T12:00:00.000Z",
      "group": {
        "id": "string",
        "links": {
          "self": "https://example.com"
        },
        "recipientType": "string",
        "status": "string",
        "targetName": "Ava Chen"
      },
      "id": "string",
      "member": {
        "firstName": "Ava",
        "id": "string",
        "lastName": "Chen",
        "links": {
          "self": "https://example.com"
        },
        "recipientType": "string",
        "status": "string",
        "targetName": "Ava Chen"
      },
      "replacement": {
        "firstName": "Ava",
        "id": "string",
        "lastName": "Chen",
        "links": {
          "self": "https://example.com"
        },
        "recipientType": "string",
        "status": "string",
        "targetName": "Ava Chen"
      },
      "start": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `absenceType` | string |  |
| `end` | date |  |
| `group.id` | string |  |
| `group.links.self` | string |  |
| `group.recipientType` | string |  |
| `group.status` | string |  |
| `group.targetName` | string |  |
| `id` | string |  |
| `member.firstName` | string |  |
| `member.id` | string |  |
| `member.lastName` | string |  |
| `member.links.self` | string |  |
| `member.recipientType` | string |  |
| `member.status` | string |  |
| `member.targetName` | string |  |
| `replacement.firstName` | string |  |
| `replacement.id` | string |  |
| `replacement.lastName` | string |  |
| `replacement.links.self` | string |  |
| `replacement.recipientType` | string |  |
| `replacement.status` | string |  |
| `replacement.targetName` | string |  |
| `start` | date |  |

## Native endpoint

Through the native xMatters API, this operation is `DELETE temporary-absences/{temporaryAbsenceId}` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-a-temporary-absence.md) for the provider-specific parameters and requirements.

