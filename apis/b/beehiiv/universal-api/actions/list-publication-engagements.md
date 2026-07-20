# Beehiiv: List Publication Engagements

Retrieves publication engagements from Beehiiv.

```
GET https://connect.mindcloud.co/v1/universal/beehiiv/latest/actions/list-publication-engagements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beehiiv `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beehiiv/latest/actions/list-publication-engagements?connectionId=$CONNECTION_ID&publicationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "publicationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beehiiv/latest/actions/list-publication-engagements?${params}`, {
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
| `publicationId` | string | yes | The prefixed ID of the publication object. |
| `startDate` | string | no | The starting date in YYYY-MM-DD format. |
| `numberOfDays` | number | no | Number of days to return metrics for (1-31). |
| `granularity` | string | no | Granularity for reported metrics. |
| `emailType` | string | no | Filter engagement by email type. |
| `direction` | string | no | Sort direction (asc or desc). |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Beehiiv API returns.

## Native endpoint

Through the native Beehiiv API, this operation is `GET /v2/publications/:publicationId/engagements` (base URL `https://api.beehiiv.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-publication-engagements.md) for the provider-specific parameters and requirements.

