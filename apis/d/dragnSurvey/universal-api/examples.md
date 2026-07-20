# Drag'n Survey Universal API Examples

These examples use the MindCloud API key and Drag'n Survey connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Surveys

Retrieves available surveys from Drag'n Survey.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dragnSurvey/latest/actions/list-surveys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dragnSurvey/latest/actions/list-surveys?${params}`, {
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

See the full [List Surveys action reference](actions/list-surveys.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dragnSurvey/latest/actions/list-surveys).

## Create Collector Custom Links

Creates respondent identification links for a Drag'n Survey collector.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dragnSurvey/latest/actions/create-collector-custom-links" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dragnSurvey/latest/actions/create-collector-custom-links', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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

See the full [Create Collector Custom Links action reference](actions/create-collector-custom-links.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dragnSurvey/latest/actions/create-collector-custom-links).
