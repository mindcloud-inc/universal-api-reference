# SMSINDIAHUB (India) Universal API Examples

These examples use the MindCloud API key and SMSINDIAHUB (India) connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Balance



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSINDIAHUBIndia/latest/actions/check-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSINDIAHUBIndia/latest/actions/check-balance?${params}`, {
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
      "rawResponse": "string"
    }
  ],
  "meta": {}
}
```

See the full [Check Balance action reference](actions/check-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sMSINDIAHUBIndia/latest/actions/check-balance).

## Schedule Promotional SMS



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sMSINDIAHUBIndia/latest/actions/schedule-promotional-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "msisdn": "string",
  "sid": "string",
  "msg": "string",
  "schedtime": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sMSINDIAHUBIndia/latest/actions/schedule-promotional-sms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "msisdn": "string",
    "sid": "string",
    "msg": "string",
    "schedtime": "string"
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
      "ErrorCode": "string",
      "ErrorMessage": "string",
      "JobId": "string",
      "MessageData": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Schedule Promotional SMS action reference](actions/schedule-promotional-sms.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sMSINDIAHUBIndia/latest/actions/schedule-promotional-sms).
