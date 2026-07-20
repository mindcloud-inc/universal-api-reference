# Test Campaign with Moosend

Tests a campaign in Moosend.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns/{{CampaignID}}/send-test.json`
- **Base URL:** `https://api.moosend.com/v3`
- **Official documentation:** [Test Campaign](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54601-Test-a-campaign?lang=en_US)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CampaignID` | path | `string` | yes | The ID of the draft campaign that you want to test. |
| `TestEmails` | body | `list<object>` | yes | A list of email addresses that you want to use to send your test campaign. Use a comma (,) to separate up to a maximum of five email addresses. |
