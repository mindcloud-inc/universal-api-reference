# Infobip Universal API Examples

These examples use the MindCloud API key and Infobip connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Outbound SMS Delivery Reports



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/infobip/latest/actions/get-outbound-sms-delivery-reports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/infobip/latest/actions/get-outbound-sms-delivery-reports?${params}`, {
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
      "results": {
        "bulkId": "string",
        "callbackData": "string",
        "campaignReferenceId": "string",
        "doneAt": "2026-05-07T12:00:00.000Z",
        "error": {
          "description": "string",
          "groupId": 1,
          "groupName": "Ava Chen",
          "id": 1,
          "name": "Ava Chen",
          "permanent": true
        },
        "mccMnc": "string",
        "messageCount": 1,
        "messageId": "string",
        "platform": {
          "applicationId": "string",
          "entityId": "string"
        },
        "price": {
          "currency": "string",
          "pricePerMessage": 1
        },
        "sender": "string",
        "sentAt": "2026-05-07T12:00:00.000Z",
        "status": {
          "action": "string",
          "description": "string",
          "groupId": 1,
          "groupName": "Ava Chen",
          "id": 1,
          "name": "Ava Chen"
        },
        "to": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Outbound SMS Delivery Reports action reference](actions/get-outbound-sms-delivery-reports.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/infobip/latest/actions/get-outbound-sms-delivery-reports).

## Add Email Domain



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/infobip/latest/actions/add-email-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domainName": "Ava Chen",
  "targetedDailyTraffic": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/infobip/latest/actions/add-email-domain', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domainName": "Ava Chen",
    "targetedDailyTraffic": 1
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
      "active": true,
      "blocked": true,
      "blocklistConfigurationLevel": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dnsRecords": {
        "expectedValue": "string",
        "name": "Ava Chen",
        "recordType": "string",
        "verified": true
      },
      "domainId": 1,
      "domainName": "Ava Chen",
      "tracking": {
        "clicks": true,
        "opens": true,
        "unsubscribe": true
      }
    }
  ],
  "meta": {}
}
```

See the full [Add Email Domain action reference](actions/add-email-domain.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/infobip/latest/actions/add-email-domain).
