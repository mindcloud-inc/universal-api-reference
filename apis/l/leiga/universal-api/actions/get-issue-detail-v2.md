# Leiga: Get Issue Detail V2

Retrieves detailed issue information from Leiga.

```
GET https://connect.mindcloud.co/v1/universal/leiga/latest/actions/get-issue-detail-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leiga `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leiga/latest/actions/get-issue-detail-v2?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leiga/latest/actions/get-issue-detail-v2?${params}`, {
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
| `id` | number | yes | Issue ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createBy": {},
      "createTime": 1,
      "fields": {},
      "id": 1,
      "issueNumber": "string",
      "issueType": {},
      "multiFields": {},
      "projectId": 1,
      "singleFields": {},
      "updateBy": {},
      "updateTime": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createBy` | object |  |
| `createTime` | number |  |
| `fields` | object |  |
| `id` | number |  |
| `issueNumber` | string |  |
| `issueType` | object |  |
| `multiFields` | object |  |
| `projectId` | number |  |
| `singleFields` | object |  |
| `updateBy` | object |  |
| `updateTime` | number |  |

## Native endpoint

Through the native Leiga API, this operation is `GET /issue/v2/get` (base URL `https://app.leiga.com/openapi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-issue-detail-v2.md) for the provider-specific parameters and requirements.

