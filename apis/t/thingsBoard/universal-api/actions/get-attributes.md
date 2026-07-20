# ThingsBoard: Get Attributes

Retrieves attributes for a specific entity from ThingsBoard.

```
GET https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/get-attributes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ThingsBoard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/get-attributes?connectionId=$CONNECTION_ID&entityType=string&entityId=string&params=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entityType": "string",
  "entityId": "string",
  "params": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/get-attributes?${params}`, {
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
| `entityType` | string | yes | The ThingsBoard entity type, for example DEVICE. |
| `entityId` | string | yes | The ThingsBoard entity ID. |
| `params` | string | yes | Additional provider-specific telemetry query parameters. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "": [
        {
          "key": "string",
          "lastUpdateTs": 1,
          "value": true
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `[].key` | string |  |
| `[].lastUpdateTs` | number |  |
| `[].value` | boolean |  |

## Native endpoint

Through the native ThingsBoard API, this operation is `GET /plugins/telemetry/:entityType/:entityId/values/attributes` (base URL `{{credentials.baseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-attributes.md) for the provider-specific parameters and requirements.

