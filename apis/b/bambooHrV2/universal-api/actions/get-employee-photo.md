# BambooHR: Get Employee Photo

Retrieves employee photo from BambooHR.

```
GET https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/get-employee-photo
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BambooHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/get-employee-photo?connectionId=$CONNECTION_ID&employeeId=1&size=large" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "employeeId": "1",
  "size": "large"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/get-employee-photo?${params}`, {
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
| `employeeId` | number | yes | The ID of the employee whose photo to retrieve. |
| `size` | list<string> | yes | The desired photo size. One of: `original`, `large`, `medium`, `small`, `xs`, `tiny`. One of: `large`, `medium`, `original`, `small`, `tiny`, `xs`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `width` | number | no | Optional. Scales the returned image to the specified pixel width, capped at the natural width of the requested size. Only applies to `small` and `tiny` sizes. |
| `height` | number | no | Optional. Scales the returned image to the specified pixel height, capped at the natural height of the requested size. Only applies to `small` and `tiny` sizes. |
| `ifNoneMatch` | string | no | Optional. The `ETag` value from a previous response for this same photo. If it still matches, the server returns `304 Not Modified` with no body instead of re-sending the image. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BambooHR API returns.

## Native endpoint

Through the native BambooHR API, this operation is `GET /v1/employees/:employeeId/photo/:size` (base URL `https://{{credentials.companyDomain}}.bamboohr.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-employee-photo.md) for the provider-specific parameters and requirements.

