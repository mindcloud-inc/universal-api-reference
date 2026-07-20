# OfficeClip: List Tracker Cases

Retrieves tracker cases from OfficeClip.

```
GET https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/list-tracker-cases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OfficeClip `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/list-tracker-cases?connectionId=$CONNECTION_ID&limit=25&offset=0&binderSid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "binderSid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/list-tracker-cases?${params}`, {
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
| `binderSid` | string | yes | Required OfficeClip tracker binder id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "assignedTo": "string",
          "caseId": "string",
          "createdDate": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "name": "Ava Chen",
          "status": "string"
        }
      ],
      "pagination": {
        "first": "string",
        "last": "string",
        "next": "string",
        "prev": "string",
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].assignedTo` | string |  |
| `data[].caseId` | string |  |
| `data[].createdDate` | date |  |
| `data[].id` | string |  |
| `data[].name` | string |  |
| `data[].status` | string |  |
| `pagination.first` | string |  |
| `pagination.last` | string |  |
| `pagination.next` | string |  |
| `pagination.prev` | string |  |
| `pagination.total` | number |  |

## Native endpoint

Through the native OfficeClip API, this operation is `GET /api/tracker-case-summary` (base URL `https://app.officeclip.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tracker-cases.md) for the provider-specific parameters and requirements.

