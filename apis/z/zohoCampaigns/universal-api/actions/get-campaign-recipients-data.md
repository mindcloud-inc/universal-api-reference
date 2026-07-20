# Zoho Campaigns: Get Campaign Recipients Data

Retrieves campaign recipient data from Zoho Campaigns.

```
GET https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/get-campaign-recipients-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Campaigns `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/get-campaign-recipients-data?connectionId=$CONNECTION_ID&campaignKey=f70c4878c4a47169407e63917ad24497&action=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignKey": "f70c4878c4a47169407e63917ad24497",
  "action": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/get-campaign-recipients-data?${params}`, {
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
| `campaignKey` | string | yes | Campaign key from a recent-campaign response. Example: `f70c4878c4a47169407e63917ad24497`. |
| `action` | string | yes | Recipient subset to fetch for the campaign. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyname": "Ava Chen",
      "contactemailaddress": "ava@example.com",
      "contactid": "string",
      "contactstatus": "string",
      "firstname": "Ava",
      "lastname": "Chen",
      "phone": "string",
      "sentdate": "string",
      "sentTime": "string",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyname` | string | Recipient company name. |
| `contactemailaddress` | string | Recipient email address. |
| `contactid` | string | Zoho contact identifier. |
| `contactstatus` | string | Zoho contact status for the recipient. |
| `firstname` | string | Recipient first name. |
| `lastname` | string | Recipient last name. |
| `phone` | string | Recipient phone number. |
| `sentdate` | string | Formatted sent date returned by Zoho. |
| `sentTime` | string | Sent timestamp in epoch milliseconds. |
| `timezone` | string | Recipient timezone string when available. |

## Native endpoint

Through the native Zoho Campaigns API, this operation is `POST /getcampaignrecipientsdata` (base URL `https://campaigns.zoho.com/api/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-recipients-data.md) for the provider-specific parameters and requirements.

