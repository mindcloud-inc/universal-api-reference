# Encodian - Convert Universal API Examples

These examples use the MindCloud API key and Encodian - Convert connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get an Operation Status

Retrieves an operation status from Encodian - Convert.

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

Example response:

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

See the full [Get an Operation Status action reference](actions/conversion-get-operation-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/encodianConvert/latest/actions/conversion-get-operation-status).

## Convert - CAD

Creates a converted file from a CAD file in Encodian - Convert.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encodianConvert/latest/actions/convert-cad" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "outputFormatParameter": "string",
  "outputFilename": "Ava Chen",
  "fileName": "Ava Chen",
  "fileContent": "string",
  "outputFormat": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodianConvert/latest/actions/convert-cad', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "outputFormatParameter": "string",
    "outputFilename": "Ava Chen",
    "fileName": "Ava Chen",
    "fileContent": "string",
    "outputFormat": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

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

See the full [Convert - CAD action reference](actions/convert-cad.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/encodianConvert/latest/actions/convert-cad).
