# Ninetailed: Evaluate Profile



```
GET https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/evaluate-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ninetailed `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/evaluate-profile?connectionId=$CONNECTION_ID&events%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "events[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/evaluate-profile?${params}`, {
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
| `events[]` | array<object> | yes | Events to evaluate for the profile request. |
| `locale` | string | no | ISO 639-1 language code used for experience evaluation. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ninetailed API returns.

## Native endpoint

Through the native Ninetailed API, this operation is `POST /v2/organizations/:organizationId/environments/:environmentSlug/profiles` (base URL `https://api.contentful.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/evaluate-profile.md) for the provider-specific parameters and requirements.

