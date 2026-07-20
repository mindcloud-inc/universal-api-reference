# CampaignKit Universal API Examples

These examples use the MindCloud API key and CampaignKit connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate Emails

Validates one or more email addresses in CampaignKit.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campaignKit/latest/actions/validate-emails?connectionId=$CONNECTION_ID&emails%5B%5D=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "emails[]": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campaignKit/latest/actions/validate-emails?${params}`, {
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
      "creditsUsed": 1,
      "results": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

See the full [Validate Emails action reference](actions/validate-emails.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/campaignKit/latest/actions/validate-emails).

## Create Validation Job

Creates a bulk email validation job in CampaignKit.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/campaignKit/latest/actions/create-validation-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "source": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/campaignKit/latest/actions/create-validation-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "source": "0"
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
      "id": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Validation Job action reference](actions/create-validation-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/campaignKit/latest/actions/create-validation-job).
