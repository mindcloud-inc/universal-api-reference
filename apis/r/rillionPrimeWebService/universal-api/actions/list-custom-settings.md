# Rillion Prime Web Service: List Custom Settings

List custom settings in Rillion Prime. Administrative operation.

```
GET https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/list-custom-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Web Service `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/list-custom-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/list-custom-settings?${params}`, {
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
| `sCompany` | list<string> | no | Company to filter by. |
| `sType` | string | no | Setting type to filter by. |
| `sSetting` | string | no | Setting name to filter by. |
| `sValue` | string | no | Setting value to filter by. |
| `companyIsNull` | boolean | no | When true, only return settings that have no company. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime Web Service API returns.

## Native endpoint

Through the native Rillion Prime Web Service API, this operation is `POST` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-custom-settings.md) for the provider-specific parameters and requirements.

