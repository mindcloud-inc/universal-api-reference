# Federal Communications Commission: List Folder History

Retrieves FCC OPIF folder change history.

```
GET https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/list-folder-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Federal Communications Commission `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/list-folder-history?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/list-folder-history?${params}`, {
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
| `count` | string | no | Number of folders in the list. |
| `endDate` | string | no | End date in YYYY-MM-DD format. |
| `entityId` | string | no | Unique entity ID. |
| `format` | string | no | Response format. FCC documents json, jsonp, xml. |
| `offset` | string | no | Starting row number. |
| `startDate` | string | no | Start date in YYYY-MM-DD format. |
| `status` | string | no | Folder status filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "history": [
        {}
      ],
      "status": "string",
      "statusCode": 1,
      "statusMessage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `history` | array<object> | Folder history rows. |
| `status` | string | FCC Manager response status. |
| `statusCode` | number | FCC Manager response status code. |
| `statusMessage` | string | FCC Manager response message. |

## Native endpoint

Through the native Federal Communications Commission API, this operation is `GET /api/manager/folder/history.{format}` (base URL `https://publicfiles.fcc.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-folder-history.md) for the provider-specific parameters and requirements.

