# Maildrip: Get an email by ID for a specific campaign



```
GET https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-an-email-by-id-for-a-specific-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-an-email-by-id-for-a-specific-campaign?connectionId=$CONNECTION_ID&campaignId=string&emailId=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string",
  "emailId": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-an-email-by-id-for-a-specific-campaign?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | ID of the campaign |
| `emailId` | string | yes | ID of the email |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | object |  |

## Native endpoint

Through the native Maildrip API, this operation is `GET /api/v1/campaigns/{campaignId}/{emailId}` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-an-email-by-id-for-a-specific-campaign.md) for the provider-specific parameters and requirements.

