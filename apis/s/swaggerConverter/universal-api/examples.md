# Swagger Converter Universal API Examples

These examples use the MindCloud API key and Swagger Converter connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Convert Definition by URL

Retrieves a converted OpenAPI document from Swagger Converter by source URL.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/swaggerConverter/latest/actions/convert-definition-by-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fpetstore.swagger.io%2Fv2%2Fswagger.json" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://petstore.swagger.io/v2/swagger.json"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/swaggerConverter/latest/actions/convert-definition-by-url?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Convert Definition by URL action reference](actions/convert-definition-by-url.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/swaggerConverter/latest/actions/convert-definition-by-url).

## Convert Definition by Content

Creates a converted OpenAPI document in Swagger Converter from input content.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/swaggerConverter/latest/actions/convert-definition-by-content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "specification": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/swaggerConverter/latest/actions/convert-definition-by-content', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "specification": {}
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

See the full [Convert Definition by Content action reference](actions/convert-definition-by-content.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/swaggerConverter/latest/actions/convert-definition-by-content).
