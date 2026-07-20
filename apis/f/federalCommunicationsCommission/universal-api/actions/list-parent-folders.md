# Federal Communications Commission: List Parent Folders

Retrieves FCC OPIF parent folders.

```
GET https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/list-parent-folders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Federal Communications Commission `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/list-parent-folders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/list-parent-folders?${params}`, {
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
| `entityId` | string | no | Unique entity ID. |
| `format` | string | no | Response format. FCC documents json, jsonp, xml. |
| `sourceService` | string | no | Source service code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "folders": [
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
| `folders` | array<object> | Parent folders. |
| `status` | string | FCC Manager response status. |
| `statusCode` | number | FCC Manager response status code. |
| `statusMessage` | string | FCC Manager response message. |

## Native endpoint

Through the native Federal Communications Commission API, this operation is `GET /api/manager/folder/parentFolders.{format}` (base URL `https://publicfiles.fcc.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-parent-folders.md) for the provider-specific parameters and requirements.

