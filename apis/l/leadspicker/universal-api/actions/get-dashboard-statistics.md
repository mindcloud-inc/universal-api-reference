# Leadspicker: Get Dashboard Statistics

Retrieves dashboard statistics from Leadspicker.

```
GET https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/get-dashboard-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadspicker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/get-dashboard-statistics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/get-dashboard-statistics?${params}`, {
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
| `timeFrame` | string | no | Dashboard time frame filter. |
| `customStartDate` | date | no | Dashboard custom start date. |
| `customEndDate` | date | no | Dashboard custom end date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chart_data": {},
      "emails_replied": 1,
      "emails_replied_change": 1,
      "emails_sent": 1,
      "emails_sent_change": 1,
      "linkedin_already_connected": 1,
      "linkedin_already_connected_change": 1,
      "linkedin_connections_accepted": 1,
      "linkedin_connections_accepted_change": 1,
      "linkedin_connections_accepted_rate": 1,
      "linkedin_connections_accepted_rate_change": 1,
      "linkedin_connections_sent": 1,
      "linkedin_connections_sent_change": 1,
      "linkedin_follows_sent": 1,
      "linkedin_follows_sent_change": 1,
      "linkedin_inmails_replied": 1,
      "linkedin_inmails_replied_change": 1,
      "linkedin_inmails_sent": 1,
      "linkedin_inmails_sent_change": 1,
      "linkedin_messages_replied": 1,
      "linkedin_messages_replied_change": 1,
      "linkedin_messages_sent": 1,
      "linkedin_messages_sent_change": 1,
      "total_active_projects": 1,
      "total_active_projects_change": 1,
      "total_eligible_leads": 1,
      "total_eligible_leads_change": 1,
      "total_finished_leads": 1,
      "total_finished_leads_change": 1,
      "total_messages_sent": 1,
      "total_messages_sent_change": 1,
      "total_person_reached": 1,
      "total_person_reached_change": 1,
      "total_replies": 1,
      "total_replies_change": 1,
      "total_reply_rate": 1,
      "total_reply_rate_change": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chart_data` | object |  |
| `emails_replied` | number |  |
| `emails_replied_change` | number |  |
| `emails_sent` | number |  |
| `emails_sent_change` | number |  |
| `linkedin_already_connected` | number |  |
| `linkedin_already_connected_change` | number |  |
| `linkedin_connections_accepted` | number |  |
| `linkedin_connections_accepted_change` | number |  |
| `linkedin_connections_accepted_rate` | number |  |
| `linkedin_connections_accepted_rate_change` | number |  |
| `linkedin_connections_sent` | number |  |
| `linkedin_connections_sent_change` | number |  |
| `linkedin_follows_sent` | number |  |
| `linkedin_follows_sent_change` | number |  |
| `linkedin_inmails_replied` | number |  |
| `linkedin_inmails_replied_change` | number |  |
| `linkedin_inmails_sent` | number |  |
| `linkedin_inmails_sent_change` | number |  |
| `linkedin_messages_replied` | number |  |
| `linkedin_messages_replied_change` | number |  |
| `linkedin_messages_sent` | number |  |
| `linkedin_messages_sent_change` | number |  |
| `total_active_projects` | number |  |
| `total_active_projects_change` | number |  |
| `total_eligible_leads` | number |  |
| `total_eligible_leads_change` | number |  |
| `total_finished_leads` | number |  |
| `total_finished_leads_change` | number |  |
| `total_messages_sent` | number |  |
| `total_messages_sent_change` | number |  |
| `total_person_reached` | number |  |
| `total_person_reached_change` | number |  |
| `total_replies` | number |  |
| `total_replies_change` | number |  |
| `total_reply_rate` | number |  |
| `total_reply_rate_change` | number |  |

## Native endpoint

Through the native Leadspicker API, this operation is `GET /app/sb/api/dashboard/stats` (base URL `https://app.leadspicker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dashboard-statistics.md) for the provider-specific parameters and requirements.

