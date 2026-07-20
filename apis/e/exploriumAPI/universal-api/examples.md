# Explorium Universal API Examples

These examples use the MindCloud API key and Explorium connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Active Credits Summary

Retrieves active credits summary from Explorium API.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/exploriumAPI/latest/actions/get-active-credits-summary?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/exploriumAPI/latest/actions/get-active-credits-summary?${params}`, {
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
      "allocatedCredits": 1,
      "remainingCredits": 1,
      "responseContext": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Active Credits Summary action reference](actions/get-active-credits-summary.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/exploriumAPI/latest/actions/get-active-credits-summary).

## Add Businesses Enrollments

Adds business event enrollments in Explorium API.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/exploriumAPI/latest/actions/add-businesses-enrollments" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "business_ids[]": [
    "string"
  ],
  "enrollment_key": "string",
  "event_types[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/exploriumAPI/latest/actions/add-businesses-enrollments', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "business_ids[]": ["string"],
    "enrollment_key": "string",
    "event_types[]": ["string"]
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
      "responseContext": {}
    }
  ],
  "meta": {}
}
```

See the full [Add Businesses Enrollments action reference](actions/add-businesses-enrollments.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/exploriumAPI/latest/actions/add-businesses-enrollments).
