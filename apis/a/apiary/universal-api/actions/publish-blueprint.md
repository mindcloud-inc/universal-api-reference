# Apiary: Publish Blueprint

Publishes an API blueprint in Apiary.

```
PUT https://connect.mindcloud.co/v1/universal/apiary/latest/actions/publish-blueprint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apiary `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/apiary/latest/actions/publish-blueprint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "apiName": "mindcloudapp",
  "code": "string",
  "shouldCommit": "no"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/apiary/latest/actions/publish-blueprint', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "apiName": "mindcloudapp",
    "code": "string",
    "shouldCommit": "no"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `apiName` | string | yes | Select the Apiary API subdomain to publish blueprint source to. Example: `mindcloudapp`. |
| `code` | string | yes | Full API Blueprint source to publish. |
| `messageToSave` | string | no | Commit message shown in Apiary history. Default: `Saving API Description Document from MindCloud`. |
| `shouldCommit` | string | yes | Apiary publish flag. Use `yes` to commit or `no` for the current publish behavior. One of: `0`, `1`. Default: `no`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Apiary API returns.

## Native endpoint

Through the native Apiary API, this operation is `POST /blueprint/publish/{{apiName}}` (base URL `https://api.apiary.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-blueprint.md) for the provider-specific parameters and requirements.

