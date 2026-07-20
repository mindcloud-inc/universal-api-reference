# Avoma: List Notes

Retrieves notes from Avoma.

```
GET https://connect.mindcloud.co/v1/universal/avoma/latest/actions/list-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avoma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avoma/latest/actions/list-notes?connectionId=$CONNECTION_ID&fromDate=string&toDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fromDate": "string",
  "toDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avoma/latest/actions/list-notes?${params}`, {
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
| `fromDate` | string | yes | Retrieve notes for meetings started at or after this UTC datetime. Use ISO 8601. |
| `toDate` | string | yes | Retrieve notes for meetings started at or before this UTC datetime. Use ISO 8601. |
| `pageSize` | number | no | Number of records returned per response. Default: `5`. |
| `outputFormat` | string | no | Format of notes to return: json, html, or markdown. Default: `json`. |
| `meetingUuid` | string | no | Unique ID of the meeting for which notes will be fetched. |
| `customCategory` | string | no | Unique ID of the custom category to filter notes by. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "data": [
        {}
      ],
      "modified": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `data` | array<object> |  |
| `modified` | date |  |

## Native endpoint

Through the native Avoma API, this operation is `GET /v1/notes/` (base URL `https://api.avoma.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-notes.md) for the provider-specific parameters and requirements.

