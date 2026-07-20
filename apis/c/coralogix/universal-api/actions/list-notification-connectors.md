# Coralogix: List Notification Connectors



```
GET https://connect.mindcloud.co/v1/universal/coralogix/latest/actions/list-notification-connectors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coralogix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coralogix/latest/actions/list-notification-connectors?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coralogix/latest/actions/list-notification-connectors?${params}`, {
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
| `connectorType` | string | no | Optional connector_type query parameter supported by the Coralogix OpenAPI endpoint. |
| `supportedByEntityType` | string | no | Optional supported_by_entity_type query parameter supported by the Coralogix OpenAPI endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "connectors": [
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
| `connectors` | array<object> | connectors returned by Coralogix. |

## Native endpoint

Through the native Coralogix API, this operation is `GET /notifications/notification-center/v1/connectors` (base URL `https://api.eu2.coralogix.com/mgmt/openapi/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-notification-connectors.md) for the provider-specific parameters and requirements.

