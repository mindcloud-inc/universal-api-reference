# SuperSend: Get Team Cost Allocation

Retrieves team cost allocation from SuperSend.

```
GET https://connect.mindcloud.co/v1/universal/superSend/latest/actions/get-team-cost-allocation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/get-team-cost-allocation?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superSend/latest/actions/get-team-cost-allocation?${params}`, {
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
| `period` | number | no | Default: 0. Range: 0 to 6. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allocation_method": "string",
      "org_totals": {
        "contacts": 1,
        "credits_used": 1,
        "domains": 1,
        "email_senders": 1,
        "emails_sent": 1,
        "mailboxes": 1,
        "monthly_cost": 1
      },
      "periods": [
        {
          "end": "string",
          "index": 1,
          "label": "string",
          "start": "string"
        }
      ],
      "selected_period": {
        "end": "string",
        "index": 1,
        "label": "string",
        "start": "string"
      },
      "social_senders": {
        "by_team": [
          {
            "linkedin_senders": 1,
            "team_id": "string",
            "team_name": "Ava Chen",
            "twitter_senders": 1
          }
        ],
        "linkedin_senders": 1,
        "twitter_senders": 1
      },
      "teams": [
        {
          "allocated_cost": 1,
          "contacts": 1,
          "credits_used": 1,
          "domain_cost": 1,
          "domains": 1,
          "email_senders": 1,
          "emails_pct": 1,
          "emails_sent": 1,
          "mailbox_cost": 1,
          "mailboxes": 1,
          "team_id": "string",
          "team_name": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allocation_method` | string |  |
| `org_totals.contacts` | number |  |
| `org_totals.credits_used` | number |  |
| `org_totals.domains` | number |  |
| `org_totals.email_senders` | number |  |
| `org_totals.emails_sent` | number |  |
| `org_totals.mailboxes` | number |  |
| `org_totals.monthly_cost` | number |  |
| `periods[].end` | string |  |
| `periods[].index` | number |  |
| `periods[].label` | string |  |
| `periods[].start` | string |  |
| `selected_period.end` | string |  |
| `selected_period.index` | number |  |
| `selected_period.label` | string |  |
| `selected_period.start` | string |  |
| `social_senders.by_team[].linkedin_senders` | number |  |
| `social_senders.by_team[].team_id` | string |  |
| `social_senders.by_team[].team_name` | string |  |
| `social_senders.by_team[].twitter_senders` | number |  |
| `social_senders.linkedin_senders` | number |  |
| `social_senders.twitter_senders` | number |  |
| `teams[].allocated_cost` | number |  |
| `teams[].contacts` | number |  |
| `teams[].credits_used` | number |  |
| `teams[].domain_cost` | number |  |
| `teams[].domains` | number |  |
| `teams[].email_senders` | number |  |
| `teams[].emails_pct` | number |  |
| `teams[].emails_sent` | number |  |
| `teams[].mailbox_cost` | number |  |
| `teams[].mailboxes` | number |  |
| `teams[].team_id` | string |  |
| `teams[].team_name` | string |  |

## Native endpoint

Through the native SuperSend API, this operation is `GET /billing/team-usage` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team-cost-allocation.md) for the provider-specific parameters and requirements.

