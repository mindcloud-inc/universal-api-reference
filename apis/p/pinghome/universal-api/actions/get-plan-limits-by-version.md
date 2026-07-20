# Pinghome: Get Plan Limits By Version

Retrieves plan limits from Pinghome by version.

```
GET https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/get-plan-limits-by-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinghome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/get-plan-limits-by-version?connectionId=$CONNECTION_ID&plan=string&version=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "plan": "string",
  "version": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/get-plan-limits-by-version?${params}`, {
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
| `plan` | string | yes | The plan identifier, such as team, developer, or business. |
| `version` | string | yes | The plan version identifier, for example v1. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pinghome API returns.

## Native endpoint

Through the native Pinghome API, this operation is `GET https://customer-query.api.pinghome.io/v1/plan/:plan/:version/limits` (base URL `https://api.pinghome.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-plan-limits-by-version.md) for the provider-specific parameters and requirements.

