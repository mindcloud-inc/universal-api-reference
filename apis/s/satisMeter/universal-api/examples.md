# SatisMeter Universal API Examples

These examples use the MindCloud API key and SatisMeter connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Project



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/satisMeter/latest/actions/get-project?connectionId=$CONNECTION_ID&projectId=61fce0adea447e24ec27d606" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "61fce0adea447e24ec27d606"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/satisMeter/latest/actions/get-project?${params}`, {
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
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Project action reference](actions/get-project.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/satisMeter/latest/actions/get-project).

## Insert NPS Survey Response



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/satisMeter/latest/actions/insert-nps-survey-response" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "writeKey": "string",
  "userId": "string",
  "score": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/satisMeter/latest/actions/insert-nps-survey-response', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "writeKey": "string",
    "userId": "string",
    "score": 1
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

See the full [Insert NPS Survey Response action reference](actions/insert-nps-survey-response.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/satisMeter/latest/actions/insert-nps-survey-response).
