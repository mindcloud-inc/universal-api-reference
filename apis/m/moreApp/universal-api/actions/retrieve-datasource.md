# MoreApp: Retrieve Datasource

Retrieves a datasource from MoreApp.

```
GET https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/retrieve-datasource
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/retrieve-datasource?connectionId=$CONNECTION_ID&customerId=1&dataSourceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1",
  "dataSourceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/retrieve-datasource?${params}`, {
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
| `customerId` | number | yes | MoreApp customer ID. |
| `dataSourceId` | string | yes | Datasource ID. |

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

Through the native MoreApp API, this operation is `GET /api/v1.0/customers/{{customerId}}/datasources/{{dataSourceId}}` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-datasource.md) for the provider-specific parameters and requirements.

