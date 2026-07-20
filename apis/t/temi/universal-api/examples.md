# Temi Universal API Examples

These examples use the MindCloud API key and Temi connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Details

Retrieves Temi account details.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/temi/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/temi/latest/actions/get-account-details?${params}`, {
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
      "balance": 1,
      "email": "ava@example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get Account Details action reference](actions/get-account-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/temi/latest/actions/get-account-details).

## Create Job

Creates a transcription job in Temi.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/temi/latest/actions/create-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mediaUrl": "https://example.com/audio.wav"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/temi/latest/actions/create-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mediaUrl": "https://example.com/audio.wav"
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
      "created_on": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "metadata": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Job action reference](actions/create-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/temi/latest/actions/create-job).
