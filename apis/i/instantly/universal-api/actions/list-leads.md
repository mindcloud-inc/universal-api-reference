# Instantly: List Leads

Retrieve leads from your Instantly workspace with advanced search filters.

```
GET https://connect.mindcloud.co/v1/universal/instantly/latest/actions/list-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instantly `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instantly/latest/actions/list-leads?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instantly/latest/actions/list-leads?${params}`, {
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
| `queries[].actionType` | list<string> | no | Available options: `reply`, `email-open`, `last-contacted`, `link-click`, `lead-status`, `lead-status-change` |
| `queries[].values.leadStatus.condition` | list<string> | no | Available options: `is`, `is-not` Example: `is-not`. |
| `queries[].values.occurrenceCount.condition` | list<string> | no | Available options: "more", "less", "equal" |
| `queries[].values.occurrenceDays` | number | no | The specified `actionType` occurred within the last x-days. Example: "link-click" within the last `14` days. |
| `search` | string | no | Example: "John Doe" Search term matched against the lead's email and profile fields (first and last name, company, job title, and similar). - Matches whole words, and the beginning of a field's value. - "smith" finds "John Smith" - "mith" does not. - Provide `campaign` or `list_id` to also match inside values. Example: `John Doe`. |
| `filter` | list<string> | no | Filter criteria for leads. For custom lead labels, use the `interest_status` field. Here is the complete list of supported `filter` values formatted as tables, grouped by category: ### 1. Campaign & Sequence Status \| Value \| Label \| Description \| \| :--- \| :--- \| :--- \| \| `FILTER_VAL_CONTACTED` \| Contacted \| Leads that have received at least one email in the campaign. \| \| `FILTER_VAL_NOT_CONTACTED` \| Not Yet Contacted \| Leads uploaded to the campaign that haven't been emailed yet. \| \| `FILTER_VAL_ACTIVE` \| Active \| Leads currently in progress and active in the sequence. \| \| `FILTER_VAL_COMPLETED` \| Completed \| Leads that completed all scheduled steps in the sequence. \| \| `FILTER_VAL_IN_SUBSEQUENCE` \| In Subsequence \| Leads branched into and running in a subsequence. \| \| `FILTER_VAL_UNSUBSCRIBED` \| Unsubscribed \| Leads that clicked unsubscribe or requested to opt out. \| \| `FILTER_VAL_BOUNCED` \| Bounced \| Leads whose email delivery resulted in a hard or soft bounce. \| \| `FILTER_VAL_SKIPPED` \| Skipped \| Leads skipped from sending by BounceShield or safety rules. \| --- ### 2. Engagement & Activity \| Value \| Label \| Description \| \| :--- \| :--- \| :--- \| \| `FILTER_VAL_REPLIED` \| Reply Received \| Leads that have sent at least one email reply. \| \| `FILTER_VAL_LINK_CLICKED` \| Link Clicked \| Leads that clicked a tracked link within an outreach email. \| \| `FILTER_VAL_OPENED_NO_REPLY` \| Email Opened, No Reply \| Leads that opened one or more emails but have not replied. \| \| `FILTER_VAL_COMPLETED_NO_REPLY` \| Completed, No Reply \| Leads that finished the entire sequence without ever replying. \| \| `FILTER_VAL_NO_OPENS` \| No Email Opened \| Leads that were contacted but have not opened any emails. \| --- ### 3. Email Verification Status \| Value \| Label \| Description \| \| :--- \| :--- \| :--- \| \| `FILTER_VAL_VALID` \| Valid \| Leads whose email addresses were verified as safe and deliverable. \| \| `FILTER_VAL_INVALID` \| Invalid \| Leads verified as invalid, dead, or non-deliverable addresses. \| \| `FILTER_VAL_RISKY` \| Risky \| Leads identified as catch-all, accept-all, or low-confidence deliverability. \| --- ### 4. CRM & Lead Interest Status \| Value \| Label \| Description \| \| :--- \| :--- \| :--- \| \| `FILTER_LEAD_INTERESTED` \| Interested \| Leads marked with positive interest. \| \| `FILTER_LEAD_NOT_INTERESTED` \| Not Interested \| Leads marked as not interested in the offer. \| \| `FILTER_LEAD_MEETING_BOOKED` \| Meeting Booked \| Leads that scheduled or agreed to a meeting. \| \| `FILTER_LEAD_MEETING_COMPLETED` \| Meeting Completed \| Leads with whom a scheduled meeting has taken place. \| \| `FILTER_LEAD_CLOSED` \| Closed / Won \| Opportunities successfully closed or won. \| \| `FILTER_LEAD_OUT_OF_OFFICE` \| Out of Office \| Leads whose reply was identified as an automated out-of-office message. \| \| `FILTER_LEAD_WRONG_PERSON` \| Wrong Person \| Leads who indicated they are not the appropriate contact. \| \| `FILTER_LEAD_LOST` \| Lost \| Deals or opportunities marked as lost. \| \| `FILTER_LEAD_NO_SHOW` \| No Show \| Prospects who did not attend a scheduled meeting. \| \| `FILTER_LEAD_CUSTOM_LABEL_POSITIVE` \| Custom Positive Label \| Leads tagged with any workspace custom label set to positive interest. \| \| `FILTER_LEAD_CUSTOM_LABEL_NEGATIVE` \| Custom Negative Label \| Leads tagged with any workspace custom label set to negative interest. \| |
| `queries[].values` | object | no | **Example: replied within the last `7` days, more than `2` times.** - actionType: "reply" - occurrence-days: 7 - occurrence-count.condition: "more" - occurrence-count.count: 2 **Example: opened an email within the last `14` days, more than `3` times.** - actionType: "email-open" - occurrence-days: 14 - occurrence-count.condition: "more" - occurrence-count.count: 3 **Example: contacted within the last `5` days.** - actionType: "last-contacted" - occurrence-days: 5 **Example: clicked a link within the last `10` days, more than `1` time.** - actionType: "link-click" - occurrence-days: 10 - occurrence-count.condition: "more" - occurrence-count.count: 1 **Example: lead status is Interested.** - actionType: "lead-status" - lead-status.status: 1 - lead-status.condition: "is" **Example: lead status changed within the last `3` days, and is Not Interested.** - actionType: "lead-status-change" - occurrence-days: 3 - lead-status.status: -1 - lead-status.condition: "is" |
| `queries[].values.leadStatus.status` | list<number> | no | Enter a numeric status code: Numeric Code (status) Status Label Category Description 1 Interested Positive Prospect indicated interest in your offer 2 Meeting Booked Positive Prospect scheduled a meeting/call 3 Meeting Completed Positive Meeting took place 4 Closed Positive Deal won / customer converted 0 Out of Office Neutral Auto-responder or out-of-office message received -1 Not Interested Negative Prospect explicitly declined or passed -2 Wrong Person Negative Contact indicated they are not the relevant person -3 Lost Negative Deal lost / opportunity closed without conversion -4 No Show Negative Prospect missed scheduled meeting Example: `1`. |
| `queries[].values.occurrenceCount` | object | no | How many times did the 'actionType' occur? Example: "more" than `2` times |
| `queries[].values.occurrenceCount.count` | number | no | Example: 2 Example: `2`. |
| `campaign` | string | no | Campaign ID to filter leads. Example: `01a0d07f-2f8a-73da-9cb3-5b898b7773d6`. |
| `queries[].values.leadStatus` | object | no |  |
| `listId` | string | no | List ID to filter leads. Example: `01a0d07f-2f8a-73da-9cb3-5b8ad8458a8d`. |
| `smartViewId` | string | no | Smart view ID to filter leads. Example: `01a0d07f-4085-7940-8b9d-476c02cc4e69`. |
| `enrichmentStatus` | list<number> | no | Enrichment status to filter leads. Available options: `1`, `-1`, `11`, `-2` Here is what each numeric enum value means: Value Status Name Description 1 Enriched The lead has been successfully enriched with additional contact/company data. -1 No Data The enrichment process ran, but no matching enrichment data was found for this lead. 11 Pending The enrichment job is currently queued or in progress. -2 Error An error occurred while attempting to enrich the lead. |
| `esgCode` | list<string> | no | ESG code to filter leads. Available options(string): `0`, `1`, `2`, `3`, `4`, `all`, `none` |
| `inList` | boolean | no | Whether the lead is in a list. (true / false) |
| `inCampaign` | boolean | no | Whether the lead is in a campaign. |
| `isWebsiteVisitor` | boolean | no | Whether the lead is a website visitor |
| `distinctContacts` | boolean | no | Whether to return distinct contacts. - true(toggled on): don't return duplicate leads. - false(toggled off): show all leads, including duplicates. |
| `ids[]` | array<string> | no | One or more lead IDs to include |
| `excludedIds[]` | array<string> | no | One or more lead IDs to exclude. |
| `contacts[]` | array<string> | no | One or more emails the leads needs to have. |
| `organizationUserIDs[]` | array | no | One or more organization user IDs to filter leads. |
| `queries[]` | array<object> | no | Find & segment leads based on activity or status, using one or more query conditions Each query requires an `actionType` and a `value` Example: Find leads who have - reply: within last 14-days, more than 2-times - reply: within last 14-days, more than 1-times AND link-click: within last 7 days more than 1-time - email-open: within last 30-days, more than 3-times - last-contacted: within last 90-days - link-click: within last 7-days, more than 1-time - lead-status: is "Interested" - lead-status-change: within last 7-days, to "Not Interested" |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `startingAfter` | string | no | Forward pagination cursor. When `distinct_contacts` is: - `false`, provide the `id` value from the last lead of the previous page; - `true`, provide the lead's email. |
| `limit` | number | no | Number of leads to return. Example: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyDomain": "string",
      "companyName": "Ava Chen",
      "email": "ava@example.com",
      "emailClickCount": 1,
      "emailOpenCount": 1,
      "emailReplyCount": 1,
      "espCode": 1,
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "listId": "string",
      "organization": "string",
      "payload": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "lastName": "Chen"
      },
      "personalization": "string",
      "status": 1,
      "timestampCreated": "string",
      "timestampUpdated": "string",
      "uploadMethod": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyDomain` | string |  |
| `companyName` | string |  |
| `email` | string |  |
| `emailClickCount` | number |  |
| `emailOpenCount` | number |  |
| `emailReplyCount` | number |  |
| `espCode` | number |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `listId` | string |  |
| `organization` | string |  |
| `payload.email` | string |  |
| `payload.firstName` | string |  |
| `payload.lastName` | string |  |
| `personalization` | string |  |
| `status` | number |  |
| `timestampCreated` | string |  |
| `timestampUpdated` | string |  |
| `uploadMethod` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Instantly API, this operation is `POST /api/v2/leads/list` (base URL `https://api.instantly.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-leads.md) for the provider-specific parameters and requirements.

