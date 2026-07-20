# Federal Communications Commission: Get File Details

Retrieves FCC OPIF file details by file ID.

```
GET https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/get-file-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Federal Communications Commission `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/get-file-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/get-file-details?${params}`, {
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
| `fileId` | string | no | Unique ID of the file. |
| `format` | string | no | Response format. FCC documents json, jsonp, xml. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "file": {},
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
| `file` | object | File details. |
| `status` | string | FCC Manager response status. |
| `statusCode` | number | FCC Manager response status code. |
| `statusMessage` | string | FCC Manager response message. |

## Native endpoint

Through the native Federal Communications Commission API, this operation is `GET /api/manager/file/id/{fileId}.{format}` (base URL `https://publicfiles.fcc.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file-details.md) for the provider-specific parameters and requirements.

