# Edusign: Get Course ID By API ID

Retrieves a course ID from Edusign by API ID.

```
GET https://connect.mindcloud.co/v1/universal/edusign/latest/actions/get-course-id-by-api-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/edusign/latest/actions/get-course-id-by-api-id?connectionId=$CONNECTION_ID&apiId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "apiId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/edusign/latest/actions/get-course-id-by-api-id?${params}`, {
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
| `apiId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {
        "id": "string"
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object |  |
| `result.id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Edusign API, this operation is `GET /v1/course/get-id/:apiId` (base URL `https://ext.edusign.fr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-course-id-by-api-id.md) for the provider-specific parameters and requirements.

