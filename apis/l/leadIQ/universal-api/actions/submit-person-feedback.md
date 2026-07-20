# LeadIQ: Submit Person Feedback



```
PUT https://connect.mindcloud.co/v1/universal/leadIQ/latest/actions/submit-person-feedback
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LeadIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/leadIQ/latest/actions/submit-person-feedback" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leadIQ/latest/actions/submit-person-feedback', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `personId` | string | no | LeadIQ person identifier for the contact you are reporting feedback about. |
| `value` | string | yes | The corrected email address or phone number value you are submitting feedback for. |
| `status` | list | no | Contact info status. Allowed values: Correct or Invalid. One of: `Correct`, `Invalid`. |
| `type` | list | no | Contact info type. Common values include WorkEmail, WorkPhone, PersonalEmail, and PersonalPhone. One of: `Fax`, `PersonalEmail`, `PersonalLandline`, `PersonalMobile`, `PersonalPhone`, `WorkBranch`, `WorkEmail`, `WorkHQ`, `WorkMobile`, `WorkPhone`. |
| `linkedinUrl` | string | no | LinkedIn profile URL for the person you are reporting feedback about. |
| `linkedinId` | string | no | LinkedIn member ID for the person you are reporting feedback about. |
| `name` | string | no | Name of the person the feedback refers to. |
| `companyId` | string | no | LeadIQ company identifier associated with the person. |
| `companyName` | string | no | Company name associated with the person. |
| `companyDomain` | string | no | Company domain associated with the person. |
| `title` | string | no | Job title associated with the person. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invalidReason` | string | no | Reason the value is invalid. Use one of LeadIQ's InvalidReason enum values such as WrongPerson or Other. |
| `lastSeen` | date | no | When the contact value was last seen, as an ISO date-time. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native LeadIQ API returns.

## Native endpoint

Through the native LeadIQ API, this operation is `POST graphql` (base URL `https://api.leadiq.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-person-feedback.md) for the provider-specific parameters and requirements.

