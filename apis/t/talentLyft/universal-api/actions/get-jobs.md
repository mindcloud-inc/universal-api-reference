# TalentLyft: Get Jobs

Retrieves all jobs from TalentLyft.

```
GET https://connect.mindcloud.co/v1/universal/talentLyft/latest/actions/get-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentLyft `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/talentLyft/latest/actions/get-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/talentLyft/latest/actions/get-jobs?${params}`, {
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
| `page` | number | no | Page number to return. |
| `perPage` | number | no | Number of results to return per page. |
| `contains` | string | no | Filter jobs whose title contains this value. |
| `sort` | string | no | Sort order for the jobs list. |
| `details` | boolean | no | Whether to include job details and description fields. |
| `includeStages` | boolean | no | Whether to include job stages in each result. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TalentLyft API returns.

## Native endpoint

Through the native TalentLyft API, this operation is `GET /v2/jobs` (base URL `https://api.talentlyft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-jobs.md) for the provider-specific parameters and requirements.

