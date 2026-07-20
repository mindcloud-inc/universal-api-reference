# Tricentis qTest: Query Object Histories

Finds object histories in Tricentis qTest by query criteria.

```
GET https://connect.mindcloud.co/v1/universal/tricentisQTest/latest/actions/query-object-histories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tricentis qTest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tricentisQTest/latest/actions/query-object-histories?connectionId=$CONNECTION_ID&projectId=1&body=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1",
  "body": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tricentisQTest/latest/actions/query-object-histories?${params}`, {
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
| `projectId` | number | yes | ID of the qTest project. |
| `body` | object | yes | Object history query body including object_type and filter criteria. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "actor": {},
      "created_date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "object_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string |  |
| `actor` | object |  |
| `created_date` | date |  |
| `id` | number |  |
| `object_type` | string |  |

## Native endpoint

Through the native Tricentis qTest API, this operation is `POST /projects/{projectId}/histories` (base URL `https://mindcloudapps.qtestnet.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-object-histories.md) for the provider-specific parameters and requirements.

