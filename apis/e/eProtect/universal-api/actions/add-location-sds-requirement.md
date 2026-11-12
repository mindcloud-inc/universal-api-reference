# 3E Protect: Add Location SDS Requirement



```
POST https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/add-location-sds-requirement
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 3E Protect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/add-location-sds-requirement" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "obtainment": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/add-location-sds-requirement', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "obtainment": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `obtainment` | object | yes | SDS obtainment (sourcing) language and country for this location. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `obtainment.locale` | string | no | Two-letter language code, such as en. Use a language configured in List SDS Requirements. Example: `en`. |
| `obtainment.country` | string | no | Three-letter country code, such as USA. Use a country configured in List SDS Requirements. Example: `USA`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 3E Protect API returns.

## Native endpoint

Through the native 3E Protect API, this operation is `POST /location-obtainment` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-location-sds-requirement.md) for the provider-specific parameters and requirements.

