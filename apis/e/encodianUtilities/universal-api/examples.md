# Encodian - Utilities Universal API Examples

These examples use the MindCloud API key and Encodian - Utilities connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Utilities - Array Add Items



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodianUtilities/latest/actions/utilities-array-add-items?connectionId=$CONNECTION_ID&data=string&items=string&itemPosition=Last" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "data": "string",
  "items": "string",
  "itemPosition": "Last"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodianUtilities/latest/actions/utilities-array-add-items?${params}`, {
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
      "errors": [
        "string"
      ],
      "httpStatusCode": 1,
      "httpStatusMessage": "string",
      "operationId": "string",
      "operationStatus": "string",
      "result": "string"
    }
  ],
  "meta": {}
}
```

See the full [Utilities - Array Add Items action reference](actions/utilities-array-add-items.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/encodianUtilities/latest/actions/utilities-array-add-items).

## Utilities - Create GUID



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encodianUtilities/latest/actions/utilities-create-guid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "case": "Lower"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodianUtilities/latest/actions/utilities-create-guid', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "case": "Lower"
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
      "errors": [
        "string"
      ],
      "httpStatusCode": 1,
      "httpStatusMessage": "string",
      "operationId": "string",
      "operationStatus": "string",
      "result": "string"
    }
  ],
  "meta": {}
}
```

See the full [Utilities - Create GUID action reference](actions/utilities-create-guid.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/encodianUtilities/latest/actions/utilities-create-guid).
