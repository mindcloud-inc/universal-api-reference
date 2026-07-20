# Moosend: Create Draft Campaign

Creates a draft campaign in Moosend.

```
POST https://connect.mindcloud.co/v1/universal/moosend/latest/actions/create-draft-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moosend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moosend/latest/actions/create-draft-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "subject": "string",
  "senderEmail": "ava@example.com",
  "replyToEmail": "ava@example.com",
  "isAb": true,
  "abCampaignType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moosend/latest/actions/create-draft-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "subject": "string",
    "senderEmail": "ava@example.com",
    "replyToEmail": "ava@example.com",
    "isAb": true,
    "abCampaignType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name of the campaign. |
| `campaignType` | string | no | You can set the campaign type to "Regular" or "Transactional". |
| `subject` | string | yes | The subject line of the campaign. |
| `senderEmail` | string | yes | The email address of the campaign sender. |
| `replyToEmail` | string | yes | The email address selected to receive replies from the campaign. This must be one of your campaign senders. If not specified, the SenderEmail is assumed. |
| `confirmationToEmail` | string | no | The email address used to send a confirmation message when the campaign has been successfully sent. This can be any valid email address. If not specified, the SenderEmail is assumed. |
| `htmlContent` | string | no | The complete HTML body of the campaign. You can use this parameter instead of using the WebLocation parameter. |
| `webLocation` | string | no | The URL used to retrieve the HTML content of the campaign. Moosend automatically moves all CSS inline. |
| `mailingLists` | list<object> | no | A list of email lists in your account that is used to send the campaign. |
| `segmentId` | string | no | The ID of a segment in the selected email list. If not specified, the campaign is sent to all active subscribers of the email list. |
| `isAb` | boolean | yes | A flag that defines if a campaign is an A/B split campaign. If true , you must fill out A/B split campaign parameters . |
| `trackInGoogleAnalytics` | boolean | no | Specifies if tracking is enabled for the campaign. You must have Google Analytics configured on your site to use this feature. |
| `abCampaignType` | string | yes | Specify the type of test to be performed in the AB split campaign to determine the winning version: Subjectline - test two different versions of the subject line. Content - test two different versions of the campaign content. Sender - test two different versions of the campaign sender. |
| `subjectB` | string | no | If testing A/B split campaigns with two subject line versions, this is the second subject version of the subject. |
| `htmlContentB` | string | no | If testing A/B split campaigns with two HTML content versions, this is the complete HTML body of the second version. |
| `webLocationB` | string | no | If testing A/B split campaigns with two HTML content versions, this is the web location of the second HTML content version. |
| `senderEmailB` | string | no | If testing A/B split campaigns with two sender versions, this is the email address of the second campaign sender. This must be one of the senders defined in your account. |
| `hoursToTest` | number | no | Specify how long the test runs, before determining the winning campaign version to be sent to the rest of the recipients. This must be an integer between 1 and 24. |
| `listPercentage` | number | no | Specifies a portion of the target recipients to get the test campaign versions. For example, if you specify 10, then 10% of your recipients receive campaign A and another 10% receive the campaign B version. This must be an integer between 5 and 40. |
| `abWinnerSelectionType` | string | no | Specifies the method to determine the winning version for the test. If not set, OpenRate is assumed. OpenRate - determine the winner based on the version that achieved more opens. TotalUniqueClicks - determine the winner based on the version that achieved more unique link clicks. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native Moosend API, this operation is `POST /campaigns/create.json` (base URL `https://api.moosend.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-draft-campaign.md) for the provider-specific parameters and requirements.

