# Mona AI Universal API Examples

These examples use the MindCloud API key and Mona AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check API Key Validity

Checks whether a Mona AI API key is valid.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/check-api-key-validity?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/check-api-key-validity?${params}`, {
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
      "message": "string",
      "valid": true
    }
  ],
  "meta": {}
}
```

See the full [Check API Key Validity action reference](actions/check-api-key-validity.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/monaAI/latest/actions/check-api-key-validity).
