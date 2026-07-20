# Moderation API Universal API Examples

These examples use the MindCloud API key and Moderation API connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Details

Retrieves account details from Moderation API.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/get-account-details?${params}`, {
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
      "current_project": {},
      "id": "string",
      "paid_plan_name": "Ava Chen",
      "remaining_quota": 1,
      "text_api_quota": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Account Details action reference](actions/get-account-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/moderationAPI/latest/actions/get-account-details).

## Add Words To Wordlist

Adds words to a wordlist in Moderation API.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/add-words-to-wordlist" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "words[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/add-words-to-wordlist', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "words[]": ["string"]
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
      "addedCount": 1,
      "addedWords": [
        "string"
      ],
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

See the full [Add Words To Wordlist action reference](actions/add-words-to-wordlist.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/moderationAPI/latest/actions/add-words-to-wordlist).
