# SARE: List Group Emails

Retrieves subscriber email addresses from a SARE group.

```
GET https://connect.mindcloud.co/v1/universal/sARE/latest/actions/list-group-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SARE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sARE/latest/actions/list-group-emails?connectionId=$CONNECTION_ID&group=1&page=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "group": "1",
  "page": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sARE/latest/actions/list-group-emails?${params}`, {
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
| `group` | number | yes | Group identifier from the SARE account. |
| `page` | number | yes | Zero-based page number for the SARE route. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SARE API returns.

## Native endpoint

Through the native SARE API, this operation is `GET /group/emails/:group/:page` (base URL `https://s.enewsletter.pl/api/v1/{{credentials.uid}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-group-emails.md) for the provider-specific parameters and requirements.

