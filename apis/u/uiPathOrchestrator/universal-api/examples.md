# UiPath Orchestrator Universal API Examples

These examples use the MindCloud API key and UiPath Orchestrator connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get asset



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/get-asset?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/get-asset?${params}`, {
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
      "BoolValue": true,
      "Id": 1,
      "IntValue": 1,
      "Name": "Ava Chen",
      "StringValue": "string",
      "Value": "string",
      "ValueScope": "string",
      "ValueType": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get asset action reference](actions/get-asset.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/uiPathOrchestrator/latest/actions/get-asset).

## Create asset



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/create-asset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "valueScope": "Global",
  "valueType": "Text"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/create-asset', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "valueScope": "Global",
    "valueType": "Text"
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
      "Id": 1,
      "Name": "Ava Chen",
      "Value": "string",
      "ValueScope": "string",
      "ValueType": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create asset action reference](actions/create-asset.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/uiPathOrchestrator/latest/actions/create-asset).
