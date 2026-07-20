# Rev AI Universal API Examples

These examples use the MindCloud API key and Rev AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account

Retrieves account details from Rev AI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/revAI/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/revAI/latest/actions/get-account?${params}`, {
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
      "balanceSeconds": 1,
      "email": "ava@example.com",
      "freeBalance": 1,
      "hipaaEnabled": true,
      "purchasedBalance": 1,
      "totalBalance": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Account action reference](actions/get-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/revAI/latest/actions/get-account).

## Create Custom Vocabulary

Creates a custom vocabulary in Rev AI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/revAI/latest/actions/create-custom-vocabulary" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customVocabularies[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/revAI/latest/actions/create-custom-vocabulary', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customVocabularies[]": [{}]
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
      "callbackUrl": "https://example.com",
      "completedOn": "string",
      "createdOn": "string",
      "failure": "string",
      "failureDetail": "string",
      "id": "string",
      "metadata": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Custom Vocabulary action reference](actions/create-custom-vocabulary.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/revAI/latest/actions/create-custom-vocabulary).
