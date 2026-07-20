# Tabidoo: Create Development App From Production App

Creates a development app from a production app in Tabidoo.

```
POST https://connect.mindcloud.co/v1/universal/tabidoo/latest/actions/create-development-app-from-production-app
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tabidoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tabidoo/latest/actions/create-development-app-from-production-app" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "applicationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tabidoo/latest/actions/create-development-app-from-production-app', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "applicationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `applicationId` | string | yes | The production Tabidoo application ID to clone into a DEV app. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `overrideExistingTemplateId` | string | no | Optional template ID required when the production app was already linked to a previous DEV template and you want to force creating a new DEV app. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Tabidoo API returns.

## Native endpoint

Through the native Tabidoo API, this operation is `POST /templates/createDevAppFromProdApp` (base URL `https://app.tabidoo.cloud/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-development-app-from-production-app.md) for the provider-specific parameters and requirements.

