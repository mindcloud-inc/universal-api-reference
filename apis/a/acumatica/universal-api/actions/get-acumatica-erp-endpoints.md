# Acumatica: List Acumatica Endpoints

Retrieve the Acumatica ERP Endpoints and the build version.

```
GET https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-acumatica-erp-endpoints
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-acumatica-erp-endpoints?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-acumatica-erp-endpoints?${params}`, {
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
| `unusedParam` | list<string> | no | Choose what data to retrieve in the response. Accepted values are 'version' (to retrieve the Acumatica ERP version) and 'endpoints' to retrieve the endpoints. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endpoints": [
        {
          "href": "string",
          "name": "Ava Chen",
          "version": "string"
        }
      ],
      "version": {
        "acumaticaBuildVersion": "string",
        "databaseVersion": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endpoints[].href` | string |  |
| `endpoints[].name` | string |  |
| `endpoints[].version` | string |  |
| `version.acumaticaBuildVersion` | string |  |
| `version.databaseVersion` | string |  |

## Native endpoint

Through the native Acumatica API, this operation is `GET /entity/` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-acumatica-erp-endpoints.md) for the provider-specific parameters and requirements.

