# Beehiiv: List Publication Email Blasts

Retrieves email blasts for a publication from Beehiiv.

```
GET https://connect.mindcloud.co/v1/universal/beehiiv/latest/actions/list-publication-email-blasts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beehiiv `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beehiiv/latest/actions/list-publication-email-blasts?connectionId=$CONNECTION_ID&limit=25&offset=0&publicationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "publicationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beehiiv/latest/actions/list-publication-email-blasts?${params}`, {
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
| `expand[]` | array<string> | no | Optional list of expandable objects. |
| `status` | string | no | Optionally filter by email blast status. |
| `limit` | number | no | A limit on the number of objects to be returned. |
| `page` | number | no | Page number for pagination. |
| `orderBy` | string | no | The field that the results are sorted by. |
| `direction` | string | no | The direction that the results are sorted in. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Beehiiv API returns.

## Native endpoint

Through the native Beehiiv API, this operation is `GET /v2/publications/:publicationId/email_blasts` (base URL `https://api.beehiiv.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-publication-email-blasts.md) for the provider-specific parameters and requirements.

