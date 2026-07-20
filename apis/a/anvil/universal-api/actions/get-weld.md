# Anvil: Get Weld

Retrieves a single weld from Anvil.

```
GET https://connect.mindcloud.co/v1/universal/anvil/latest/actions/get-weld
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anvil `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anvil/latest/actions/get-weld?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anvil/latest/actions/get-weld?${params}`, {
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
| `variables.eid` | string | no | Provide EID for Get Weld. |
| `variables.slug` | string | no | Provide Slug for Get Weld. |
| `variables.organizationSlug` | string | no | Provide Organization Slug for Get Weld. |
| `variables.versionNumber` | number | no | Provide Version Number for Get Weld. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Anvil API returns.

## Native endpoint

Through the native Anvil API, this operation is `POST /` (base URL `https://graphql.useanvil.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-weld.md) for the provider-specific parameters and requirements.

