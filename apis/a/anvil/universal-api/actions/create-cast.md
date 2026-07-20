# Anvil: Create Cast

Creates a new cast in Anvil.

```
POST https://connect.mindcloud.co/v1/universal/anvil/latest/actions/create-cast
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anvil `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/anvil/latest/actions/create-cast" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anvil/latest/actions/create-cast', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.organizationEid` | string | no | Provide Organization EID for Create Cast. |
| `variables.title` | string | no | Provide Title for Create Cast. |
| `variables.file` | file | yes | Provide File for Create Cast. |
| `variables.isTemplate` | boolean | no | Provide Is Template for Create Cast. |
| `variables.allowedAliasIds[]` | array<string> | no | Provide Allowed Alias Ids for Create Cast. |
| `variables.detectFields` | boolean | no | Provide Detect Fields for Create Cast. |
| `variables.advancedDetectFields` | boolean | no | Provide Advanced Detect Fields for Create Cast. |
| `variables.detectBoxesAdvanced` | boolean | no | Provide Detect Boxes Advanced for Create Cast. |
| `variables.aliasIds` | object | no | Provide Alias Ids for Create Cast. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Anvil API returns.

## Native endpoint

Through the native Anvil API, this operation is `POST /` (base URL `https://graphql.useanvil.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-cast.md) for the provider-specific parameters and requirements.

