# Federal Communications Commission: List File History

Retrieves FCC OPIF file change history.

```
GET https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/list-file-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Federal Communications Commission `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/list-file-history?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/list-file-history?${params}`, {
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
| `count` | string | no | Number of files in the list. |
| `endDate` | string | no | End date in YYYY-MM-DD format. |
| `entityId` | string | no | Unique entity ID. |
| `format` | string | no | Response format. FCC documents json, jsonp, xml. |
| `offset` | string | no | Starting row number. |
| `startDate` | string | no | Start date in YYYY-MM-DD format. |
| `status` | string | no | File status filter. |

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
| `history` | array<object> | File history rows. |
| `status` | string | FCC Manager response status. |
| `statusCode` | number | FCC Manager response status code. |
| `statusMessage` | string | FCC Manager response message. |

## Native endpoint

Through the native Federal Communications Commission API, this operation is `GET /api/manager/file/history.{format}` (base URL `https://publicfiles.fcc.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-file-history.md) for the provider-specific parameters and requirements.

