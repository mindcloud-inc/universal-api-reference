# Anvil: Update Cast

Updates an existing cast in Anvil.

```
PUT https://connect.mindcloud.co/v1/universal/anvil/latest/actions/update-cast
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anvil `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/anvil/latest/actions/update-cast" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.eid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anvil/latest/actions/update-cast', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.eid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.eid` | string | yes | Provide EID for Update Cast. |
| `variables.name` | string | no | Provide Name for Update Cast. |
| `variables.title` | string | no | Provide Title for Update Cast. |
| `variables.isTemplate` | boolean | no | Provide Is Template for Update Cast. |
| `variables.organizationEid` | string | no | Provide Organization EID for Update Cast. |
| `variables.config` | object | no | Provide Config for Update Cast. |
| `variables.configFile` | file | no | Provide Config File for Update Cast. |
| `variables.file` | file | no | Provide File for Update Cast. |
| `variables.isArchived` | boolean | no | Provide Is Archived for Update Cast. |
| `variables.versionNumber` | number | no | Provide Version Number for Update Cast. |
| `variables.allowedAliasIds[]` | array<string> | no | Provide Allowed Alias Ids for Update Cast. |
| `variables.feedbackRating` | number | no | Provide Feedback Rating for Update Cast. |
| `variables.feedbackMessage` | string | no | Provide Feedback Message for Update Cast. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Anvil API returns.

## Native endpoint

Through the native Anvil API, this operation is `POST /` (base URL `https://graphql.useanvil.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-cast.md) for the provider-specific parameters and requirements.

