# Dribbble: Create Job



```
POST https://connect.mindcloud.co/v1/universal/dribbble/latest/actions/create-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dribbble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dribbble/latest/actions/create-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationName": "Ava Chen",
  "title": "string",
  "location": "string",
  "linkToApply": "https://example.com",
  "description": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dribbble/latest/actions/create-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationName": "Ava Chen",
    "title": "string",
    "location": "string",
    "linkToApply": "https://example.com",
    "description": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationName` | string | yes |  |
| `title` | string | yes |  |
| `location` | string | yes |  |
| `linkToApply` | string | yes |  |
| `description` | string | yes |  |
| `active` | boolean | no |  |
| `team` | string | no |  |
| `category` | list | no | One of: `Animator`, `Art Director`, `Brand Designer`, `Creative Director`, `Front-end Developer`, `Graphic Designer`, `Illustrator`, `Interaction Designer`, `Mobile Designer`, `Mobile Developer`, `Motion Designer`, `Other`, `Product Designer`, `UI/UX Designer`, `Web Designer`. |
| `roleType` | list | no | One of: `contract`, `freelance`, `full-time`, `part-time`. |
| `website` | string | no |  |
| `twitter` | string | no |  |
| `instagram` | string | no |  |
| `facebook` | string | no |  |
| `onsiteOrRemote` | boolean | no |  |
| `onsiteOnly` | boolean | no |  |
| `remoteOnly` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "category": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "endsAt": "2026-05-07T12:00:00.000Z",
      "facebook": "string",
      "id": 1,
      "instagram": "string",
      "linkToApply": "https://example.com",
      "location": "string",
      "organizationName": "Ava Chen",
      "roleType": "string",
      "startsAt": "2026-05-07T12:00:00.000Z",
      "team": {},
      "title": "string",
      "twitter": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `category` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `endsAt` | date |  |
| `facebook` | string |  |
| `id` | number |  |
| `instagram` | string |  |
| `linkToApply` | string |  |
| `location` | string |  |
| `organizationName` | string |  |
| `roleType` | string |  |
| `startsAt` | date |  |
| `team` | object |  |
| `title` | string |  |
| `twitter` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Dribbble API, this operation is `POST /jobs` (base URL `https://api.dribbble.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-job.md) for the provider-specific parameters and requirements.

