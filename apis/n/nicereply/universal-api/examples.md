# Nicereply Universal API Examples

These examples use the MindCloud API key and Nicereply connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Rating Values Settings

Retrieves rating value settings from Nicereply.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nicereply/latest/actions/get-rating-values-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nicereply/latest/actions/get-rating-values-settings?${params}`, {
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

See the full [Get Rating Values Settings action reference](actions/get-rating-values-settings.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nicereply/latest/actions/get-rating-values-settings).

## Assign Response Tags

Assigns a tag to a response in Nicereply.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nicereply/latest/actions/assign-response-tags" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nicereply/latest/actions/assign-response-tags', {
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

See the full [Assign Response Tags action reference](actions/assign-response-tags.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nicereply/latest/actions/assign-response-tags).
