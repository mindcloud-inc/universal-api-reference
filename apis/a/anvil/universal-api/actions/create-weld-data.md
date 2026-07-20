# Anvil: Create Weld Data

Creates new weld data in Anvil.

```
POST https://connect.mindcloud.co/v1/universal/anvil/latest/actions/create-weld-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anvil `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/anvil/latest/actions/create-weld-data" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.weldEid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anvil/latest/actions/create-weld-data', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.weldEid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.weldEid` | string | yes | Provide Weld EID for Create Weld Data. |
| `variables.weldDataGroupEid` | string | no | Provide Weld Data Group EID for Create Weld Data. |
| `variables.isTest` | boolean | no | Provide Is Test for Create Weld Data. |
| `variables.webhookURL` | string | no | Provide Webhook URL for Create Weld Data. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Anvil API returns.

## Native endpoint

Through the native Anvil API, this operation is `POST /` (base URL `https://graphql.useanvil.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-weld-data.md) for the provider-specific parameters and requirements.

