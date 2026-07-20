# Extruct AI Universal API Examples

These examples use the MindCloud API key and Extruct AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User

Retrieves the authenticated user from Extruct AI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/get-user?${params}`, {
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
      "availableCredits": 1,
      "email": "ava@example.com",
      "organizationId": {},
      "organizationIsActive": {},
      "organizationName": {},
      "organizationSlug": {},
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get User action reference](actions/get-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/extructAI/latest/actions/get-user).

## Add Input Data

Adds input data rows to a table in Extruct AI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/add-input-data" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tableId": "string",
  "rows[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/add-input-data', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tableId": "string",
    "rows[]": [{}]
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
      "company_profile_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "data": {},
      "id": "string",
      "metadata": {},
      "parent_data": {},
      "parent_row_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Input Data action reference](actions/add-input-data.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/extructAI/latest/actions/add-input-data).
