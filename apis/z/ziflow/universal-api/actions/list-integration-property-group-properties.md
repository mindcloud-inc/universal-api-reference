# Ziflow: List Integration Property Group Properties

Retrieves integration property group properties from Ziflow.

```
GET https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/list-integration-property-group-properties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ziflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/list-integration-property-group-properties?connectionId=$CONNECTION_ID&applicationKey=string&groupKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "applicationKey": "string",
  "groupKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/list-integration-property-group-properties?${params}`, {
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
| `applicationKey` | string | yes | Integration application key. |
| `groupKey` | string | yes | Integration property group key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "key": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `key` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Ziflow API, this operation is `GET /integrations/:applicationKey/property-groups/:key/properties` (base URL `https://api.ziflow.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-integration-property-group-properties.md) for the provider-specific parameters and requirements.

