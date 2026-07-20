# MerrenIO Universal API Examples

These examples use the MindCloud API key and MerrenIO connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Filter Compare And Export Responses



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/merrenIO/latest/actions/filter-compare-and-export-responses?connectionId=$CONNECTION_ID&type=question&surveyId=680000000000000000000000" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "type": "question",
  "surveyId": "680000000000000000000000"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/merrenIO/latest/actions/filter-compare-and-export-responses?${params}`, {
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

See the full [Filter Compare And Export Responses action reference](actions/filter-compare-and-export-responses.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/merrenIO/latest/actions/filter-compare-and-export-responses).

## Add Section



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/merrenIO/latest/actions/add-section" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input.title": "string",
  "input.surveyId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/merrenIO/latest/actions/add-section', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input.title": "string",
    "input.surveyId": "string"
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

See the full [Add Section action reference](actions/add-section.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/merrenIO/latest/actions/add-section).
