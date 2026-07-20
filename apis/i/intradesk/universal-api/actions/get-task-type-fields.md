# Intradesk: Get Task Type Fields

Retrieves task type fields from Intradesk.

```
GET https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/get-task-type-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intradesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/get-task-type-fields?connectionId=$CONNECTION_ID&ids=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ids": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/get-task-type-fields?${params}`, {
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
| `ids` | string | yes | One or more task type identifiers from the Intradesk TaskForm API path. Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "description": "string",
      "id": 1,
      "isAdditional": true,
      "isDefaultShow": true,
      "name": "Ava Chen",
      "sortOrder": "string",
      "taskTypeId": 1,
      "type": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string |  |
| `description` | string |  |
| `id` | number |  |
| `isAdditional` | boolean |  |
| `isDefaultShow` | boolean |  |
| `name` | string |  |
| `sortOrder` | string |  |
| `taskTypeId` | number |  |
| `type` | number |  |

## Native endpoint

Through the native Intradesk API, this operation is `GET /taskform/api/TaskTypes/{ids}/fields` (base URL `https://apigw.intradesk.ru`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task-type-fields.md) for the provider-specific parameters and requirements.

