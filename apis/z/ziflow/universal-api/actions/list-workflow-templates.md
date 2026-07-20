# Ziflow: List Workflow Templates

Retrieves workflow templates from your Ziflow account.

```
GET https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/list-workflow-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ziflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/list-workflow-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/list-workflow-templates?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "created_at": "string",
      "id": "string",
      "name": "Ava Chen",
      "owner": {
        "blocked": true,
        "company": "string",
        "email": "ava@example.com",
        "first_name": "Ava",
        "id": "string",
        "language": "string",
        "last_name": "Chen",
        "phone": "string",
        "proofing_defaults": {
          "comment": true,
          "decision": true,
          "manage": true,
          "notification": "string",
          "share": true,
          "view": true
        },
        "roles": [
          "string"
        ],
        "tenant": {
          "company_name": "Ava Chen",
          "subdomain": "string",
          "tenant_id": "string"
        },
        "timezone": "string",
        "type": "string",
        "verified": true
      },
      "permissions": {
        "add_reviewers": true,
        "add_stages": true,
        "change_reviewer_notification_preferences": true,
        "change_reviewer_roles": true,
        "change_stage_deadline": true,
        "change_stage_invitation_message": true,
        "change_stage_lock_mechanism": true,
        "change_stage_name": true,
        "change_stage_private_comments_ability": true,
        "change_stage_status_calculation": true,
        "change_stage_trigger": true,
        "remove_reviewers": true,
        "remove_stages": true
      },
      "stages": [
        {
          "allow_private_comments": true,
          "allow_public_comments": true,
          "custom_email_message": "ava@example.com",
          "custom_email_subject": "ava@example.com",
          "deadline": "string",
          "final_status_calculation": {
            "reviewer_email": "ava@example.com",
            "reviewer_id": "string",
            "type": "string"
          },
          "id": "string",
          "lock": {
            "next_stage_id": "string",
            "next_stage_name": "Ava Chen",
            "type": "string"
          },
          "name": "Ava Chen",
          "only_one_decision": true,
          "send_new_proof_email": true,
          "skip": "string",
          "skipped": true,
          "stage_previous_id": "string",
          "stage_trigger": {
            "deadline": {
              "days": 1,
              "hours": 1,
              "time": "string"
            },
            "trigger": {
              "or_deadline": true
            }
          }
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
| `active` | boolean |  |
| `created_at` | string |  |
| `id` | string |  |
| `name` | string |  |
| `owner.blocked` | boolean |  |
| `owner.company` | string |  |
| `owner.email` | string |  |
| `owner.first_name` | string |  |
| `owner.id` | string |  |
| `owner.language` | string |  |
| `owner.last_name` | string |  |
| `owner.phone` | string |  |
| `owner.proofing_defaults.comment` | boolean |  |
| `owner.proofing_defaults.decision` | boolean |  |
| `owner.proofing_defaults.manage` | boolean |  |
| `owner.proofing_defaults.notification` | string |  |
| `owner.proofing_defaults.share` | boolean |  |
| `owner.proofing_defaults.view` | boolean |  |
| `owner.roles[]` | string |  |
| `owner.tenant.company_name` | string |  |
| `owner.tenant.subdomain` | string |  |
| `owner.tenant.tenant_id` | string |  |
| `owner.timezone` | string |  |
| `owner.type` | string |  |
| `owner.verified` | boolean |  |
| `permissions.add_reviewers` | boolean |  |
| `permissions.add_stages` | boolean |  |
| `permissions.change_reviewer_notification_preferences` | boolean |  |
| `permissions.change_reviewer_roles` | boolean |  |
| `permissions.change_stage_deadline` | boolean |  |
| `permissions.change_stage_invitation_message` | boolean |  |
| `permissions.change_stage_lock_mechanism` | boolean |  |
| `permissions.change_stage_name` | boolean |  |
| `permissions.change_stage_private_comments_ability` | boolean |  |
| `permissions.change_stage_status_calculation` | boolean |  |
| `permissions.change_stage_trigger` | boolean |  |
| `permissions.remove_reviewers` | boolean |  |
| `permissions.remove_stages` | boolean |  |
| `stages[].allow_private_comments` | boolean |  |
| `stages[].allow_public_comments` | boolean |  |
| `stages[].custom_email_message` | string |  |
| `stages[].custom_email_subject` | string |  |
| `stages[].deadline` | string |  |
| `stages[].final_status_calculation.reviewer_email` | string |  |
| `stages[].final_status_calculation.reviewer_id` | string |  |
| `stages[].final_status_calculation.type` | string |  |
| `stages[].id` | string |  |
| `stages[].lock.next_stage_id` | string |  |
| `stages[].lock.next_stage_name` | string |  |
| `stages[].lock.type` | string |  |
| `stages[].name` | string |  |
| `stages[].only_one_decision` | boolean |  |
| `stages[].send_new_proof_email` | boolean |  |
| `stages[].skip` | string |  |
| `stages[].skipped` | boolean |  |
| `stages[].stage_previous_id` | string |  |
| `stages[].stage_trigger.deadline.days` | number |  |
| `stages[].stage_trigger.deadline.hours` | number |  |
| `stages[].stage_trigger.deadline.time` | string |  |
| `stages[].stage_trigger.trigger.or_deadline` | boolean |  |

## Native endpoint

Through the native Ziflow API, this operation is `GET /workflowtemplates` (base URL `https://api.ziflow.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workflow-templates.md) for the provider-specific parameters and requirements.

