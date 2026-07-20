# Whisky Hunter Universal API Examples

These examples use the MindCloud API key and Whisky Hunter connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get API Schema

Retrieves the Whisky Hunter API schema.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whiskyHunter/latest/actions/get-api-schema?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whiskyHunter/latest/actions/get-api-schema?${params}`, {
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
      "basePath": "string",
      "consumes": [
        "string"
      ],
      "definitions": {},
      "host": "string",
      "info": {},
      "paths": {},
      "produces": [
        "string"
      ],
      "schemes": [
        "string"
      ],
      "security": [
        {}
      ],
      "securityDefinitions": {},
      "swagger": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get API Schema action reference](actions/get-api-schema.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/whiskyHunter/latest/actions/get-api-schema).
