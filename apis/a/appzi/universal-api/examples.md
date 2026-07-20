# Appzi Universal API Examples

These examples use the MindCloud API key and Appzi connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Portal Survey Configurations

Retrieves portal survey configurations from Appzi.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appzi/latest/actions/list-portal-survey-configurations?connectionId=$CONNECTION_ID&portalToken=fYbQ6" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "portalToken": "fYbQ6"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appzi/latest/actions/list-portal-survey-configurations?${params}`, {
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

See the full [List Portal Survey Configurations action reference](actions/list-portal-survey-configurations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/appzi/latest/actions/list-portal-survey-configurations).

## Add Custom Feedback Data

Generates Appzi custom feedback data settings.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/appzi/latest/actions/add-custom-feedback-data" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appzi/latest/actions/add-custom-feedback-data', {
  method: 'PUT',
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

See the full [Add Custom Feedback Data action reference](actions/add-custom-feedback-data.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/appzi/latest/actions/add-custom-feedback-data).
