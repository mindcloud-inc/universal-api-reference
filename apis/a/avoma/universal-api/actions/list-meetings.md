# Avoma: List Meetings

Retrieves meetings from Avoma.

```
GET https://connect.mindcloud.co/v1/universal/avoma/latest/actions/list-meetings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avoma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avoma/latest/actions/list-meetings?connectionId=$CONNECTION_ID&fromDate=string&toDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fromDate": "string",
  "toDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avoma/latest/actions/list-meetings?${params}`, {
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
| `fromDate` | string | yes | Retrieve meetings started at or after this UTC datetime. Use ISO 8601, for example 2026-03-01T00:00:00Z. |
| `toDate` | string | yes | Retrieve meetings started at or before this UTC datetime. Use ISO 8601, for example 2026-03-18T23:59:59Z. |
| `pageSize` | number | no | Number of meetings to return per page. Default: `10`. |
| `isCall` | boolean | no | Filter for voice call meetings or video meetings. |
| `isInternal` | boolean | no | Filter for internal-only or external meetings. |
| `attendeeEmails` | string | no | Comma-separated attendee emails; meetings with any matching attendee are returned. |
| `includeCrmAssociations` | boolean | no | Include CRM associations in the response. Default: `false`. |
| `order` | string | no | Sort meetings by start time ascending or descending. Default: `-start_at`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attendees": [
        {
          "email": "ava@example.com",
          "name": "Ava Chen",
          "responseStatus": "string",
          "uuid": "string"
        }
      ],
      "created": "2026-05-07T12:00:00.000Z",
      "endAt": "2026-05-07T12:00:00.000Z",
      "modified": "2026-05-07T12:00:00.000Z",
      "organizerEmail": "ava@example.com",
      "processingStatus": "string",
      "purpose": {
        "label": "string",
        "uuid": "string"
      },
      "recordingUuid": "string",
      "startAt": "2026-05-07T12:00:00.000Z",
      "state": "string",
      "subject": "string",
      "type": {
        "label": "string",
        "uuid": "string"
      },
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attendees[].email` | string |  |
| `attendees[].name` | string |  |
| `attendees[].responseStatus` | string |  |
| `attendees[].uuid` | string |  |
| `created` | date |  |
| `endAt` | date |  |
| `modified` | date |  |
| `organizerEmail` | string |  |
| `processingStatus` | string |  |
| `purpose.label` | string |  |
| `purpose.uuid` | string |  |
| `recordingUuid` | string |  |
| `startAt` | date |  |
| `state` | string |  |
| `subject` | string |  |
| `type.label` | string |  |
| `type.uuid` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Avoma API, this operation is `GET /v1/meetings/` (base URL `https://api.avoma.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-meetings.md) for the provider-specific parameters and requirements.

