# Good Grants: Update application

Updates an existing application in Good Grants.

```
PUT https://connect.mindcloud.co/v1/universal/goodGrants/latest/actions/update-application
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Good Grants `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/goodGrants/latest/actions/update-application" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "slug": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goodGrants/latest/actions/update-application', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "slug": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `slug` | string | yes | Application slug |
| `category` | string | no | Category slug |
| `chapter` | string | no | Chapter slug |
| `applicant` | string | no | Applicant slug |
| `title` | string | no | Application title |
| `status` | string | no | Application status |
| `moderationStatus` | string | no | Moderation status |
| `grantEndDate` | date | no | Grant end date |
| `grantStatus` | string | no | Grant status slug |
| `applicationFields` | object | no | Field slug to value map |
| `customDeadline` | date | no | Custom deadline |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applicant": {},
      "application_fields": [
        {}
      ],
      "attachments": [
        {}
      ],
      "auto_score": 1,
      "category": {},
      "chapter": {},
      "comments": "string",
      "contributor_count": 1,
      "contributors": [
        {}
      ],
      "created": "2026-05-07T12:00:00.000Z",
      "custom_deadline": "string",
      "division": {},
      "eligibility_status": "string",
      "files_count": 1,
      "form": {},
      "grant_end_date": "2026-05-07T12:00:00.000Z",
      "grant_status": {},
      "local_id": 1,
      "moderation_status": "string",
      "parent_category": {},
      "payment_status": "string",
      "plagiarism_scan_status": "string",
      "review_status": "string",
      "season": {},
      "slug": "string",
      "status": "string",
      "submitted": "2026-05-07T12:00:00.000Z",
      "tags": "string",
      "title": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "user_comments": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applicant` | object |  |
| `application_fields` | array<object> |  |
| `attachments` | array<object> |  |
| `auto_score` | number |  |
| `category` | object |  |
| `chapter` | object |  |
| `comments` | string |  |
| `contributor_count` | number |  |
| `contributors` | array<object> |  |
| `created` | date |  |
| `custom_deadline` | string |  |
| `division` | object |  |
| `eligibility_status` | string |  |
| `files_count` | number |  |
| `form` | object |  |
| `grant_end_date` | date |  |
| `grant_status` | object |  |
| `local_id` | number |  |
| `moderation_status` | string |  |
| `parent_category` | object |  |
| `payment_status` | string |  |
| `plagiarism_scan_status` | string |  |
| `review_status` | string |  |
| `season` | object |  |
| `slug` | string |  |
| `status` | string |  |
| `submitted` | date |  |
| `tags` | string |  |
| `title` | string |  |
| `updated` | date |  |
| `user_comments` | string |  |

## Native endpoint

Through the native Good Grants API, this operation is `PUT application/:slug` (base URL `https://api.cr4ce.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-application.md) for the provider-specific parameters and requirements.

