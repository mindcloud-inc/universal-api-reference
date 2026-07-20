# timeBuzzer Universal API Examples

These examples use the MindCloud API key and timeBuzzer connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get My Account



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeBuzzer/latest/actions/get-my-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeBuzzer/latest/actions/get-my-account?${params}`, {
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
      "accountId": 1,
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "permissions": [
        "string"
      ],
      "state": "string",
      "templateId": 1
    }
  ],
  "meta": {}
}
```

See the full [Get My Account action reference](actions/get-my-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/timeBuzzer/latest/actions/get-my-account).

## Create Activity



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timeBuzzer/latest/actions/create-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tiles[]": [
    1
  ],
  "startDate": "string",
  "endDate": "string",
  "startUtcOffset": "string",
  "endUtcOffset": "string",
  "userId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timeBuzzer/latest/actions/create-activity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tiles[]": [1],
    "startDate": "string",
    "endDate": "string",
    "startUtcOffset": "string",
    "endUtcOffset": "string",
    "userId": 1
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
      "billed": true,
      "customData": "string",
      "endDate": "string",
      "endUtcOffset": "string",
      "id": 1,
      "lock_": {},
      "note": "string",
      "startDate": "string",
      "startUtcOffset": "string",
      "tiles": [
        1
      ],
      "userId": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Activity action reference](actions/create-activity.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/timeBuzzer/latest/actions/create-activity).
