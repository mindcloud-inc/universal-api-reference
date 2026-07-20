# Apollo: Organization Job Postings

Retrieves organization job postings from Apollo.

```
GET https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/organization-job-postings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apollo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/organization-job-postings?connectionId=$CONNECTION_ID&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/organization-job-postings?${params}`, {
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
| `organizationId` | string | yes | The organization ID of the company for which you want to find job postings. Each company in the Apollo database is assigned a unique ID. To find IDs, call the Organization Search endpoint and identify the values for `organization_id`. Example: `5e66b6381e05b4008c8331b8` |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": {},
      "country": "string",
      "id": "string",
      "lastSeenAt": "2026-05-07T12:00:00.000Z",
      "postedAt": "2026-05-07T12:00:00.000Z",
      "state": {},
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | object |  |
| `country` | string |  |
| `id` | string |  |
| `lastSeenAt` | date |  |
| `postedAt` | date |  |
| `state` | object |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Apollo API, this operation is `GET v1/organizations/:organization_id/job_postings` (base URL `https://app.apollo.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/organization-job-postings.md) for the provider-specific parameters and requirements.

