# FillFaster: Get Submissions List

Retrieves submissions for a specific FillFaster form.

```
GET https://connect.mindcloud.co/v1/universal/fillFaster/latest/actions/get-submissions-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FillFaster `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fillFaster/latest/actions/get-submissions-list?connectionId=$CONNECTION_ID&form=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "form": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fillFaster/latest/actions/get-submissions-list?${params}`, {
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
| `form` | string | yes | Form identifier to list submissions for. |
| `order` | string | no | Sort direction. |
| `page` | number | no | Results page number. |
| `sort` | string | no | Field to sort submissions by. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "publicUrl": "https://example.com",
      "sid": "string",
      "submitted": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date | Submission creation timestamp. |
| `publicUrl` | string | Public PDF URL when one exists. |
| `sid` | string | FillFaster submission identifier. |
| `submitted` | date | Submission timestamp when completed. |

## Native endpoint

Through the native FillFaster API, this operation is `GET /v1/getSubmissionsList` (base URL `https://api.fillfaster.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-submissions-list.md) for the provider-specific parameters and requirements.

