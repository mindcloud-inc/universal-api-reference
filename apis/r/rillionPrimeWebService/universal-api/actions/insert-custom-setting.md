# Rillion Prime Web Service: Insert Custom Setting

Insert a custom setting in Rillion Prime. Administrative operation — changes Prime configuration. Undocumented details: confirm with Rillion.

```
POST https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-custom-setting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Web Service `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-custom-setting" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customSettingsItem": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-custom-setting', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customSettingsItem": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customSettingsItem` | object | yes | CustomSettingsItem payload. Field semantics: Rillion Prime Integration Tables document. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime Web Service API returns.

## Native endpoint

Through the native Rillion Prime Web Service API, this operation is `POST` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/insert-custom-setting.md) for the provider-specific parameters and requirements.

