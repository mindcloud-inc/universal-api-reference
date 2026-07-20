# Stackoverflow Universal API Examples

These examples use the MindCloud API key and Stackoverflow connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Authenticated User

Retrieves the authenticated user from Stackoverflow.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID&site=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "site": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/get-authenticated-user?${params}`, {
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
      "accept_rate": 1,
      "account_id": 1,
      "display_name": "Ava Chen",
      "link": "https://example.com",
      "profile_image": "string",
      "reputation": 1,
      "user_id": 1,
      "user_type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Authenticated User action reference](actions/get-authenticated-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/stackoverflow/latest/actions/get-authenticated-user).

## Accept Answer

Accepts an existing answer in Stackoverflow.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/accept-answer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/accept-answer', {
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
  "data": [
    {
      "answer_id": 1,
      "is_accepted": true,
      "question_id": 1,
      "score": 1
    }
  ],
  "meta": {}
}
```

See the full [Accept Answer action reference](actions/accept-answer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/stackoverflow/latest/actions/accept-answer).
