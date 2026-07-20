# mails.so Universal API Examples

These examples use the MindCloud API key and mails.so connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate Email

Retrieves email validation results from mails.so.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailsso/latest/actions/validate-email?connectionId=$CONNECTION_ID&email=user%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "user@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailsso/latest/actions/validate-email?${params}`, {
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
      "avatar": "string",
      "didYouMean": "string",
      "domain": "string",
      "email": "ava@example.com",
      "id": "string",
      "isDisposable": true,
      "isFree": true,
      "isvDomain": true,
      "isvFormat": true,
      "isvMx": true,
      "isvNoblock": true,
      "isvNocatchall": true,
      "isvNogeneric": true,
      "mxRecord": "string",
      "provider": "string",
      "reason": "string",
      "result": "string",
      "score": 1,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Validate Email action reference](actions/validate-email.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mailsso/latest/actions/validate-email).

## Create Batch Validation Job

Creates a new batch validation job in mails.so.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailsso/latest/actions/create-batch-validation-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emails[]": "user@example.com,hello@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailsso/latest/actions/create-batch-validation-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emails[]": "user@example.com,hello@example.com"
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
      "createdAt": "string",
      "duration": 1,
      "finishedAt": "string",
      "id": "string",
      "name": "Ava Chen",
      "progress": 1,
      "size": 1,
      "status": "string",
      "type": "string",
      "updatedAt": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Batch Validation Job action reference](actions/create-batch-validation-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mailsso/latest/actions/create-batch-validation-job).
