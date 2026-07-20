# Docmosis Universal API Examples

These examples use the MindCloud API key and Docmosis connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Environment Summary



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/get-environment-summary?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/get-environment-summary?${params}`, {
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
      "accountEnvironmentSummary": {
        "accountEnvDetails": {
          "isActivated": true,
          "isDeleted": true,
          "isDisabled": true,
          "name": "Ava Chen"
        },
        "accountName": "Ava Chen",
        "pageQuota": {
          "isHardLimited": true,
          "pctUsed": 1,
          "pctUsedStr": "string",
          "quota": 1,
          "used": 1
        },
        "plan": {
          "name": "Ava Chen"
        },
        "ready": true
      },
      "shortMsg": "string",
      "succeeded": true
    }
  ],
  "meta": {}
}
```

See the full [Get Environment Summary action reference](actions/get-environment-summary.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/docmosis/latest/actions/get-environment-summary).

## Convert File



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/convert-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "https://files.catbox.moe/50iz06.xlsx",
  "outputName": "docmosis-convert-output.pdf"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/convert-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "https://files.catbox.moe/50iz06.xlsx",
    "outputName": "docmosis-convert-output.pdf"
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
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Convert File action reference](actions/convert-file.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/docmosis/latest/actions/convert-file).
