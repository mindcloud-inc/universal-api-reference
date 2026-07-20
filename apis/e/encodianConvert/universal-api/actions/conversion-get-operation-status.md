# Encodian - Convert: Get an Operation Status

Retrieves an operation status from Encodian - Convert.

```
GET https://connect.mindcloud.co/v1/universal/encodianConvert/latest/actions/conversion-get-operation-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - Convert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodianConvert/latest/actions/conversion-get-operation-status?connectionId=$CONNECTION_ID&operationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "operationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodianConvert/latest/actions/conversion-get-operation-status?${params}`, {
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
| `operationId` | string | yes | Retrieve the operation status for the Operation ID provided. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Errors": [
        "string"
      ],
      "FileContent": "string",
      "Filename": "Ava Chen",
      "HttpStatusCode": 1,
      "HttpStatusMessage": "string",
      "OperationId": "string",
      "OperationStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Errors` | array<string> | Errors returned by Encodian. |
| `FileContent` | string | Processed document content, usually Base64 encoded. |
| `Filename` | string | Filename of the processed document. |
| `HttpStatusCode` | number | HTTP status code returned by Encodian. |
| `HttpStatusMessage` | string | HTTP status message returned by Encodian. |
| `OperationId` | string | Unique Encodian operation ID. |
| `OperationStatus` | string | Encodian operation status. |

## Native endpoint

Through the native Encodian - Convert API, this operation is `GET /api/v1/Conversion/GetOperationStatus` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/conversion-get-operation-status.md) for the provider-specific parameters and requirements.

