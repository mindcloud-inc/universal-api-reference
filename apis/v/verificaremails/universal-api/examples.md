# Verificaremails Universal API Examples

These examples use the MindCloud API key and Verificaremails connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get All Credits

Retrieves available credits for all Verificaremails services.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verificaremails/latest/actions/get-all-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/verificaremails/latest/actions/get-all-credits?${params}`, {
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
      "apiService": "string",
      "apiServiceAlias": "string",
      "credits": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get All Credits action reference](actions/get-all-credits.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/verificaremails/latest/actions/get-all-credits).

## Create Address Batch Validation

Creates an address batch validation in Verificaremails.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/verificaremails/latest/actions/create-address-batch-validation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "column": "A"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/verificaremails/latest/actions/create-address-batch-validation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "column": "A"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Create Address Batch Validation action reference](actions/create-address-batch-validation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/verificaremails/latest/actions/create-address-batch-validation).
