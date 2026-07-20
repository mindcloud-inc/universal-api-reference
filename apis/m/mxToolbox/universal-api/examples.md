# Mx Toolbox Universal API Examples

These examples use the MindCloud API key and Mx Toolbox connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Blocklist



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mxToolbox/latest/actions/check-blocklist?connectionId=$CONNECTION_ID&target=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "target": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mxToolbox/latest/actions/check-blocklist?${params}`, {
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
      "argumentType": "string",
      "command": "string",
      "commandArgument": "string",
      "errors": [
        {}
      ],
      "failed": [
        {}
      ],
      "hasSubscriptions": true,
      "information": [
        {}
      ],
      "isEndpoint": true,
      "isError": true,
      "passed": [
        {}
      ],
      "relatedLookups": [
        {}
      ],
      "reportingNameServer": "Ava Chen",
      "resourceRecordType": 1,
      "timeouts": [
        {}
      ],
      "timeRecorded": "2026-05-07T12:00:00.000Z",
      "timeToComplete": "string",
      "transcript": [
        {}
      ],
      "uid": "string",
      "warnings": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Check Blocklist action reference](actions/check-blocklist.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mxToolbox/latest/actions/check-blocklist).
