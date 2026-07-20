# Reply Universal API Examples

These examples use the MindCloud API key and Reply connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get List of Campaigns



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reply/latest/actions/get-list-of-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reply/latest/actions/get-list-of-campaigns?${params}`, {
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
      "bouncesCount": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "deliveriesCount": 1,
      "emailAccount": "ava@example.com",
      "emailAccounts": [
        "ava@example.com"
      ],
      "id": 1,
      "name": "Ava Chen",
      "opensCount": 1,
      "optOutsCount": 1,
      "outOfOfficeCount": 1,
      "ownerEmail": "ava@example.com",
      "peopleActive": 1,
      "peopleCount": 1,
      "peopleFinished": 1,
      "peoplePaused": 1,
      "repliesCount": 1,
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [Get List of Campaigns action reference](actions/get-list-of-campaigns.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/reply/latest/actions/get-list-of-campaigns).

## Create Campaign



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/reply/latest/actions/create-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emailAccounts[]": [
    "ava@example.com"
  ],
  "name": "Ava Chen",
  "settings.dailyThrottling": 1,
  "settings.daysToFinishProspect": 1,
  "settings.disableOpensTracking": true,
  "settings.emailsCountPerDay": 1,
  "settings.emailSendingDelaySeconds": 1,
  "settings.enableLinksTracking": true,
  "settings.repliesHandlingType": "string",
  "steps[].inMinutesCount": 1,
  "steps[].number": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reply/latest/actions/create-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emailAccounts[]": ["ava@example.com"],
    "name": "Ava Chen",
    "settings.dailyThrottling": 1,
    "settings.daysToFinishProspect": 1,
    "settings.disableOpensTracking": true,
    "settings.emailsCountPerDay": 1,
    "settings.emailSendingDelaySeconds": 1,
    "settings.enableLinksTracking": true,
    "settings.repliesHandlingType": "string",
    "steps[].inMinutesCount": 1,
    "steps[].number": 1
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
      "emailAccount": "ava@example.com",
      "emailAccounts": [
        "ava@example.com"
      ],
      "id": 1,
      "name": "Ava Chen",
      "scheduleId": 1,
      "settings": {},
      "status": "string",
      "steps": [
        {}
      ],
      "useDefaultEmailAccountFallback": true
    }
  ],
  "meta": {}
}
```

See the full [Create Campaign action reference](actions/create-campaign.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/reply/latest/actions/create-campaign).
