# MoreApp: List Tasks

Retrieves tasks from MoreApp.

```
GET https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/list-tasks?connectionId=$CONNECTION_ID&customerId=209321&formId=69bc27abd8b8b4ce5be6b2ba&page=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "209321",
  "formId": "69bc27abd8b8b4ce5be6b2ba",
  "page": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/list-tasks?${params}`, {
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
| `customerId` | number | yes | MoreApp customer identifier. Default: `209321`. |
| `formId` | string | yes | MoreApp form identifier. Default: `69bc27abd8b8b4ce5be6b2ba`. |
| `page` | number | yes | Task result page number. Default: `0`. |
| `pageSize` | number | no | Optional number of tasks to return per page. Default: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "elements": [
        {}
      ],
      "totalSize": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `elements` | array<object> |  |
| `totalSize` | number |  |

## Native endpoint

Through the native MoreApp API, this operation is `POST /api/v1.0/customers/{{customerId}}/{{formId}}/tasks/filter/{{page}}` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

