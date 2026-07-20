# ClearoutPhone Universal API Examples

These examples use the MindCloud API key and ClearoutPhone connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Available Credits

Retrieves the available credits from ClearoutPhone.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clearoutPhone/latest/actions/get-available-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clearoutPhone/latest/actions/get-available-credits?${params}`, {
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
      "credits": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Available Credits action reference](actions/get-available-credits.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/clearoutPhone/latest/actions/get-available-credits).

## Create Bulk Phone Number Validation

Creates a bulk phone number validation job in ClearoutPhone.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clearoutPhone/latest/actions/create-bulk-phone-number-validation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clearoutPhone/latest/actions/create-bulk-phone-number-validation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
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
      "listId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Bulk Phone Number Validation action reference](actions/create-bulk-phone-number-validation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/clearoutPhone/latest/actions/create-bulk-phone-number-validation).
