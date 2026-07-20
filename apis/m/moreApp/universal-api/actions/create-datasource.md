# MoreApp: Create Datasource

Creates a datasource in MoreApp.

```
POST https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/create-datasource
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/create-datasource" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": 1,
  "name": "Ava Chen",
  "urlConfiguration.url": "https://example.com",
  "urlConfiguration.updateInterval": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/create-datasource', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": 1,
    "name": "Ava Chen",
    "urlConfiguration.url": "https://example.com",
    "urlConfiguration.updateInterval": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | number | yes | MoreApp customer ID. |
| `name` | string | yes | Datasource name. |
| `urlConfiguration.url` | string | yes | Source URL for URL-based datasources. |
| `urlConfiguration.updateInterval` | string | yes | Refresh interval for URL-based datasources. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "columnMapping": [
        {}
      ],
      "customerId": 1,
      "enabled": true,
      "failedExecutionCount": 1,
      "googleConfiguration": {},
      "id": "string",
      "lastSuccessfulUpdate": 1,
      "lastUpdated": 1,
      "lastUpdateType": "string",
      "lastUpdateWarningMessages": [
        "string"
      ],
      "name": "Ava Chen",
      "searchType": "string",
      "updateStatus": "string",
      "urlConfiguration": {},
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `columnMapping` | array<object> |  |
| `customerId` | number |  |
| `enabled` | boolean |  |
| `failedExecutionCount` | number |  |
| `googleConfiguration` | object |  |
| `id` | string |  |
| `lastSuccessfulUpdate` | number |  |
| `lastUpdated` | number |  |
| `lastUpdateType` | string |  |
| `lastUpdateWarningMessages` | array<string> |  |
| `name` | string |  |
| `searchType` | string |  |
| `updateStatus` | string |  |
| `urlConfiguration` | object |  |
| `version` | string |  |

## Native endpoint

Through the native MoreApp API, this operation is `POST /api/v1.0/customers/{{customerId}}/datasources` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-datasource.md) for the provider-specific parameters and requirements.

