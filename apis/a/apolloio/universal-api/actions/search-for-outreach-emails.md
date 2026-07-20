# Apollo: Search for Outreach Emails

Finds outreach emails in your Apollo account.

```
GET https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/search-for-outreach-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apollo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/search-for-outreach-emails?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/search-for-outreach-emails?${params}`, {
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
| `emailerMessageStats[]` | array<string> | no | Find emails based on their current status, such as whether they were delivered or opened. You can add multiple statuses. Possible values include: `delivered` `scheduled` `drafted` `not_opened` `opened` `clicked` `unsubscribed` `demoed` `bounced` `spam_blocked` `failed_other` |
| `emailerMessageReplyClasses[]` | array<string> | no | Find emails based on the response sentiment of the recipient. This can include the recipient expressing interest in meeting or having a follow-up question. You can add multiple values. Possible values include: `willing_to_meet` `follow_up_question` `person_referral` `out_of_office` `already_left_company_or_not_right_person` `not_interested` `unsubscribe` `none_of_the_above` |
| `userIds[]` | array<string> | no | Find emails sent by specific users in your team's Apollo account. You can add multiple users. Use the Get a List of Users endpoint to retrieve IDs for all of the users within your Apollo account. Example: `66302798d03b9601c7934ebf` |
| `emailAccountIdAndAliases` | string | no |  |
| `emailerCampaignIds[]` | array<string> | no | Search for emails that are included in specific sequences in your Apollo account. You can search multiple sequences. Any sequence not included in this parameter will be exclude from search results. To find sequence IDs, call the Search for Sequences endpoint and identify the `id` value for the sequence. Example: `66e9e215ece19801b219997f` |
| `notEmailerCampaignIds[]` | array<string> | no | Exclude emails from specific sequences in your Apollo account. You can exclude multiple sequences. Any sequence not excluded using this parameter will be included in search results. To find sequence IDs, call the Search for Sequences endpoint and identify the `id` value for the sequence. Example: `66e9e215ece19801b219997f` |
| `emailerMessageDateRangeMode` | string | no | Use this parameter in combination with the `emailer_message_date_range[max]` and `emailer_message_date_range[min]` parameters. Find emails based on 1 of the following options: `due_at`: When emails are scheduled to be delivered. `completed_at`: When emails were delivered. |
| `emailerMessageDateRange[max]` | date | no | Set the upper bound of the date range you want to search. Use this parameter in combination with the `emailer_message_date_range[min]` and `emailer_message_date_range_mode` parameters. This date should fall after the `emailer_message_date_range[min]` date. The date should be formatted as `YYYY-MM-DD`. Example: `2025-10-30` |
| `emailerMessageDateRange[min]` | date | no | Set the lower bound of the date range you want to search. Use this parameter in combination with the `emailer_message_date_range[max]` and `emailer_message_date_range_mode` parameters. This date should fall before the `emailer_message_date_range[max]` date. The date should be formatted as `YYYY-MM-DD`. Example: `2025-10-30` |
| `notSentReasonCds[]` | array<string> | no | Find emails based on the reason they were not sent. You can add multiple values. Possible values include: `contact_stage_safeguard` `same_account_reply` `account_stage_safeguard` `email_unverified` `snippets_missing` `personalized_opener_missing` `thread_reply_original_email_missing` `no_active_email_account` `email_format_invalid` `ownership_permission` `email_service_provider_delivery_failure` `sendgrid_dropped_email` `mailgun_dropped_email` `gdpr_compliance` `not_valid_hard_bounce_detected` `other_safeguard` `new_job_change_detected` `email_on_global_bounce_list` |
| `qKeywords` | string | no | Add keywords to narrow the search of the emails in your team's Apollo account. Keywords should directly match at least part of an email's content. For example, searching the keyword `James` might return emails that were sent by `James Smith`. Example: `Jane` |

## Response

```json
{
  "success": true,
  "data": [
    {
      "numFetchResult": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `numFetchResult` | object |  |

## Native endpoint

Through the native Apollo API, this operation is `GET v1/emailer_messages/search` (base URL `https://app.apollo.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-for-outreach-emails.md) for the provider-specific parameters and requirements.

