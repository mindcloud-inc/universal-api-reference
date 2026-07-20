# Kite Suite: Get WhiteBoard by project Id



```
GET https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-white-board-by-project-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-white-board-by-project-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-white-board-by-project-id?${params}`, {
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
| `id` | string | yes | Project ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "createdBy": "string",
      "isTrashed": true,
      "json": "string",
      "name": "Ava Chen",
      "projectID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | ID of the WhiteBoard |
| `createdBy` | string | creator of the this WhiteBoard |
| `isTrashed` | boolean | trash status of this WhiteBoard |
| `json` | string |  |
| `name` | string | name of WhiteBoard |
| `projectID` | string | project ID of WhiteBoard |

## Native endpoint

Through the native Kite Suite API, this operation is `GET /api/v1/white-board/project/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-white-board-by-project-id.md) for the provider-specific parameters and requirements.

