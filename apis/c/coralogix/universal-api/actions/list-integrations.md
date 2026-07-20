# Coralogix: List Integrations



```
GET https://connect.mindcloud.co/v1/universal/coralogix/latest/actions/list-integrations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coralogix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coralogix/latest/actions/list-integrations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coralogix/latest/actions/list-integrations?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeTestingRevision` | boolean | no | Optional include_testing_revision query parameter supported by the Coralogix OpenAPI endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "integrations": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `integrations` | array<object> | integrations returned by Coralogix. |

## Native endpoint

Through the native Coralogix API, this operation is `GET /integrations/integrations/v1` (base URL `https://api.eu2.coralogix.com/mgmt/openapi/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-integrations.md) for the provider-specific parameters and requirements.

