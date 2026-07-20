# Listrak Email Universal API Examples

These examples use the MindCloud API key and Listrak Email connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get List



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/listrakEmail/latest/actions/get-list?connectionId=$CONNECTION_ID&listID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/listrakEmail/latest/actions/get-list?${params}`, {
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
      "bounceDomainAlias": "string",
      "bounceHandling": "string",
      "bounceUnsubscribeCount": 1,
      "createDate": "string",
      "enableBrowserLink": true,
      "enableDoubleOptIn": true,
      "enableDynamicContent": true,
      "enableGoogleAnalytics": true,
      "enableInternationalization": true,
      "enableListHygiene": true,
      "enableListrakAnalytics": true,
      "enableListRemovalHeader": true,
      "enableListRemovalLink": true,
      "enableSpamScorePersonalization": true,
      "enableToNamePersonalization": true,
      "enableUniversalEmailKeySetting": true,
      "folderId": 1,
      "fromEmail": "ava@example.com",
      "fromName": "Ava Chen",
      "ipPoolId": 1,
      "linkDomainAlias": "https://example.com",
      "listId": 1,
      "listName": "Ava Chen",
      "mediaDomainAlias": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get List action reference](actions/get-list.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/listrakEmail/latest/actions/get-list).

## Send Transactional Email



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/listrakEmail/latest/actions/send-transactional-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": 1,
  "transactionalMessageId": 1,
  "emailAddress": "customer@example.com",
  "segmentationFieldValues[]": "[object Object]",
  "segmentationFieldValues[].segmentationFieldId": 1,
  "segmentationFieldValues[].value": "1004827"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/listrakEmail/latest/actions/send-transactional-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": 1,
    "transactionalMessageId": 1,
    "emailAddress": "customer@example.com",
    "segmentationFieldValues[]": "[object Object]",
    "segmentationFieldValues[].segmentationFieldId": 1,
    "segmentationFieldValues[].value": "1004827"
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
      "resourceId": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [Send Transactional Email action reference](actions/send-transactional-email.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/listrakEmail/latest/actions/send-transactional-email).
