# BlockSurvey Universal API Examples

These examples use the MindCloud API key and BlockSurvey connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Survey Cut Off Date

Retrieves a survey cut off date from BlockSurvey.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blockSurvey/latest/actions/get-survey-cut-off-date?connectionId=$CONNECTION_ID&surveyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blockSurvey/latest/actions/get-survey-cut-off-date?${params}`, {
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
      "scheduledStartDate": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Survey Cut Off Date action reference](actions/get-survey-cut-off-date.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/blockSurvey/latest/actions/get-survey-cut-off-date).

## Create Contact

Creates a new contact in BlockSurvey.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/blockSurvey/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "string",
  "listId": "string",
  "listPublicKey": "string",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blockSurvey/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "string",
    "listId": "string",
    "listPublicKey": "string",
    "email": "ava@example.com"
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
      "recordId": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Create Contact action reference](actions/create-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/blockSurvey/latest/actions/create-contact).
