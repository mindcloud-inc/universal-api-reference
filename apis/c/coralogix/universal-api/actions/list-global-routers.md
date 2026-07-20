# Coralogix: List Global Routers



```
GET https://connect.mindcloud.co/v1/universal/coralogix/latest/actions/list-global-routers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coralogix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coralogix/latest/actions/list-global-routers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coralogix/latest/actions/list-global-routers?${params}`, {
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
| `entityType` | string | no | Optional entity_type query parameter supported by the Coralogix OpenAPI endpoint. |
| `sourceEntityLabels` | string | no | Optional source_entity_labels query parameter supported by the Coralogix OpenAPI endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "routers": [
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
| `routers` | array<object> | routers returned by Coralogix. |

## Native endpoint

Through the native Coralogix API, this operation is `GET /notifications/notification-center/v1/routers` (base URL `https://api.eu2.coralogix.com/mgmt/openapi/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-global-routers.md) for the provider-specific parameters and requirements.

