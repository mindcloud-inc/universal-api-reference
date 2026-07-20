# Create Draft Campaign with Moosend

Creates a draft campaign in Moosend.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns/create.json`
- **Base URL:** `https://api.moosend.com/v3`
- **Official documentation:** [Create Draft Campaign](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54599-Create-a-draft-campaign?lang=en_US)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Name` | body | `string` | yes | The name of the campaign. |
| `CampaignType` | body | `string` | no | You can set the campaign type to "Regular" or "Transactional". |
| `Subject` | body | `string` | yes | The subject line of the campaign. |
| `SenderEmail` | body | `string` | yes | The email address of the campaign sender. |
| `ReplyToEmail` | body | `string` | yes | The email address selected to receive replies from the campaign. This must be one of your campaign senders. If not specified, the SenderEmail is assumed. |
| `ConfirmationToEmail` | body | `string` | no | The email address used to send a confirmation message when the campaign has been successfully sent. This can be any valid email address. If not specified, the SenderEmail is assumed. |
| `HTMLContent` | body | `string` | no | The complete HTML body of the campaign. You can use this parameter instead of using the WebLocation parameter. |
| `WebLocation` | body | `string` | no | The URL used to retrieve the HTML content of the campaign. Moosend automatically moves all CSS inline. |
| `MailingLists` | body | `list<object>` | no | A list of email lists in your account that is used to send the campaign. |
| `SegmentID` | body | `string` | no | The ID of a segment in the selected email list. If not specified, the campaign is sent to all active subscribers of the email list. |
| `IsAB` | body | `boolean` | yes | A flag that defines if a campaign is an A/B split campaign. If true , you must fill out A/B split campaign parameters . |
| `TrackInGoogleAnalytics` | body | `boolean` | no | Specifies if tracking is enabled for the campaign. You must have Google Analytics configured on your site to use this feature. |
| `ABCampaignType` | body | `string` | yes | Specify the type of test to be performed in the AB split campaign to determine the winning version: Subjectline - test two different versions of the subject line. Content - test two different versions of the campaign content. Sender - test two different versions of the campaign sender. |
| `SubjectB` | body | `string` | no | If testing A/B split campaigns with two subject line versions, this is the second subject version of the subject. |
| `HTMLContentB` | body | `string` | no | If testing A/B split campaigns with two HTML content versions, this is the complete HTML body of the second version. |
| `WebLocationB` | body | `string` | no | If testing A/B split campaigns with two HTML content versions, this is the web location of the second HTML content version. |
| `SenderEmailB` | body | `string` | no | If testing A/B split campaigns with two sender versions, this is the email address of the second campaign sender. This must be one of the senders defined in your account. |
| `HoursToTest` | body | `number` | no | Specify how long the test runs, before determining the winning campaign version to be sent to the rest of the recipients. This must be an integer between 1 and 24. |
| `ListPercentage` | body | `number` | no | Specifies a portion of the target recipients to get the test campaign versions. For example, if you specify 10, then 10% of your recipients receive campaign A and another 10% receive the campaign B version. This must be an integer between 5 and 40. |
| `ABWinnerSelectionType` | body | `string` | no | Specifies the method to determine the winning version for the test. If not set, OpenRate is assumed. OpenRate - determine the winner based on the version that achieved more opens. TotalUniqueClicks - determine the winner based on the version that achieved more unique link clicks. |
