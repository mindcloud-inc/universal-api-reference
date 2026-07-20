# Mihu AI: Get All Appointments (Calendar)



```
GET https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/get-all-appointments-calendar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mihu AI `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/get-all-appointments-calendar?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/get-all-appointments-calendar?${params}`, {
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
| `contactUuid` | string | no |  |
| `endDate` | string | no |  |
| `scheduleUuid` | string | no |  |
| `startDate` | string | no |  |
| `status` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactUuid": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "endTime": "2026-05-07T12:00:00.000Z",
      "notes": "string",
      "scheduleUuid": "string",
      "startTime": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactUuid` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `endTime` | date |  |
| `notes` | string |  |
| `scheduleUuid` | string |  |
| `startTime` | date |  |
| `status` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native Mihu AI API, this operation is `GET /api/v1/appointments` (base URL `https://{{credentials.subdomain}}.mindhunters.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-appointments-calendar.md) for the provider-specific parameters and requirements.

