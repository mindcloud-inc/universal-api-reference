# Databricks: Get Service Principal

Retrieves a service principal from the Databricks account.

```
GET https://connect.mindcloud.co/v1/universal/databricks/latest/actions/get-service-principal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Databricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/databricks/latest/actions/get-service-principal?connectionId=$CONNECTION_ID&servicePrincipalId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "servicePrincipalId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/databricks/latest/actions/get-service-principal?${params}`, {
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
| `servicePrincipalId` | string | yes | Unique ID for a service principal in the Databricks account. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$ref": "string",
      "display": "string",
      "primary": true,
      "type": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$ref` | string |  |
| `display` | string |  |
| `primary` | boolean |  |
| `type` | string |  |
| `value` | string |  |

## Native endpoint

Through the native Databricks API, this operation is `GET /api/2.0/accounts/{{credentials.accountId}}/scim/v2/ServicePrincipals/:servicePrincipalId` (base URL `https://accounts.cloud.databricks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-service-principal.md) for the provider-specific parameters and requirements.

