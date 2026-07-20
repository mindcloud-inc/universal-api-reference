# Lakera AI Guardrails Universal API Examples

These examples use the MindCloud API key and Lakera AI Guardrails connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Policy Health



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lakeraAIGuardrails/latest/actions/check-policy-health?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lakeraAIGuardrails/latest/actions/check-policy-health?${params}`, {
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
      "isDefault": true,
      "lint": {
        "errors": [
          {}
        ],
        "passed": true
      },
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Check Policy Health action reference](actions/check-policy-health.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lakeraAIGuardrails/latest/actions/check-policy-health).
