# FillFaster: List Forms

Retrieves a list of active forms from FillFaster.

```
GET https://connect.mindcloud.co/v1/universal/fillFaster/latest/actions/list-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FillFaster `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fillFaster/latest/actions/list-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fillFaster/latest/actions/list-forms?${params}`, {
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
| `order` | string | no | Sort order. Use desc or asc. |
| `page` | number | no | Results page number. FillFaster defaults to 1. |
| `sort` | string | no | Sort field. FillFaster documents created as the default. |
| `wid` | string | no | Optional workspace id when you need to scope the forms list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "fid": "string",
      "name": "Ava Chen",
      "submissions": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date | Form creation timestamp. |
| `fid` | string | FillFaster form identifier. |
| `name` | string | Form display name. |
| `submissions` | string | Submission count as returned by FillFaster. |

## Native endpoint

Through the native FillFaster API, this operation is `GET /v1/getFormsList` (base URL `https://api.fillfaster.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-forms.md) for the provider-specific parameters and requirements.

