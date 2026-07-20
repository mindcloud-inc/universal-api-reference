# Dribbble: Get Job



```
GET https://connect.mindcloud.co/v1/universal/dribbble/latest/actions/get-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dribbble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dribbble/latest/actions/get-job?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dribbble/latest/actions/get-job?${params}`, {
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
| `id` | number | yes | The Dribbble job ID. |

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

Through the native Dribbble API, this operation is `GET /jobs/:id` (base URL `https://api.dribbble.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job.md) for the provider-specific parameters and requirements.

