# GoCanvas: Retrieve Submission Value



```
GET https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/retrieve-submission-value
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCanvas `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/retrieve-submission-value?connectionId=$CONNECTION_ID&submissionId=string&valueId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "submissionId": "string",
  "valueId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/retrieve-submission-value?${params}`, {
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
| `submissionId` | string | yes | ID of the submission. |
| `valueId` | string | yes | ID of the media value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Binary file content encoded as Base64. |

## Native endpoint

Through the native GoCanvas API, this operation is `GET /submissions/:submissionId/values/:valueId` (base URL `https://www.gocanvas.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-submission-value.md) for the provider-specific parameters and requirements.

