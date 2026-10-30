# GoCanvas: List Binary Upload Statuses



```
GET https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/list-binary-upload-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCanvas `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/list-binary-upload-statuses?connectionId=$CONNECTION_ID&submissionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "submissionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/list-binary-upload-statuses?${params}`, {
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
| `submissionId` | string | yes | Numeric submission ID or mobile submission GUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentGuid": "string",
      "entryId": 1,
      "entryType": "string",
      "status": "string",
      "type": "string",
      "valueId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentGuid` | string |  |
| `entryId` | number |  |
| `entryType` | string |  |
| `status` | string |  |
| `type` | string |  |
| `valueId` | number |  |

## Native endpoint

Through the native GoCanvas API, this operation is `GET /submissions/:submissionId/values` (base URL `https://www.gocanvas.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-binary-upload-statuses.md) for the provider-specific parameters and requirements.

