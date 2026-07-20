# Pabbly Hook: Get Transformation



```
GET https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/get-transformation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Hook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/get-transformation?connectionId=$CONNECTION_ID&transformationId=trs_672cad8497fc816d4e75bc44" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transformationId": "trs_672cad8497fc816d4e75bc44"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/get-transformation?${params}`, {
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
| `transformationId` | string | yes | Transformation ID to retrieve. Example: `trs_672cad8497fc816d4e75bc44`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "Id": "string",
      "name": "Ava Chen",
      "trsId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": "string",
      "v": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Transformation JavaScript code. |
| `createdAt` | date | Creation timestamp. |
| `Id` | string | Pabbly Hook internal transformation identifier. |
| `name` | string | Transformation name. |
| `trsId` | string | Public Pabbly Hook transformation identifier. |
| `updatedAt` | date | Last update timestamp. |
| `userId` | string | Pabbly account user identifier. |
| `v` | number | Provider version counter. |

## Native endpoint

Through the native Pabbly Hook API, this operation is `GET /api/v1/transformations/:transformationId` (base URL `https://hook.pabbly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transformation.md) for the provider-specific parameters and requirements.

