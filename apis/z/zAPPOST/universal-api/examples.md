# ZAP POST Universal API Examples

These examples use the MindCloud API key and ZAP POST connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Scheduled Sends

Retrieves scheduled sends from ZAP POST.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zAPPOST/latest/actions/list-scheduled-sends?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zAPPOST/latest/actions/list-scheduled-sends?${params}`, {
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
      "Id": "string",
      "PaperStockName": "Ava Chen",
      "SendDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Scheduled Sends action reference](actions/list-scheduled-sends.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zAPPOST/latest/actions/list-scheduled-sends).

## Create Batch Submission

Creates a batch submission in a ZAP POST campaign.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zAPPOST/latest/actions/create-batch-submission" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string",
  "submissions[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zAPPOST/latest/actions/create-batch-submission', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "string",
    "submissions[]": [{}]
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

See the full [Create Batch Submission action reference](actions/create-batch-submission.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zAPPOST/latest/actions/create-batch-submission).
