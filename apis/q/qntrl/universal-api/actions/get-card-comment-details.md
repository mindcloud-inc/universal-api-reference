# Qntrl: Get Card Comment Details

Retrieves card comment details from Qntrl.

```
GET https://connect.mindcloud.co/v1/universal/qntrl/latest/actions/get-card-comment-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qntrl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qntrl/latest/actions/get-card-comment-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qntrl/latest/actions/get-card-comment-details?${params}`, {
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
| `comment_id` | string | no | Qntrl comment ID. |
| `job_id` | string | no | Qntrl card ID. |
| `org_id` | string | no | Qntrl organization ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "commentedBy": "string",
      "commentId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string |  |
| `commentedBy` | string |  |
| `commentId` | string |  |

## Native endpoint

Through the native Qntrl API, this operation is `GET /[:org_id]/job/[:job_id]/comment/[:comment_id]` (base URL `https://coreapi.qntrl.com/blueprint/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-card-comment-details.md) for the provider-specific parameters and requirements.

