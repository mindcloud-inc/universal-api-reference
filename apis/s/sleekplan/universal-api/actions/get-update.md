# Sleekplan: Get Update



```
GET https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/get-update
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sleekplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/get-update?connectionId=$CONNECTION_ID&updateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "updateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/get-update?${params}`, {
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
| `updateId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "announcement": true,
      "canDelete": true,
      "canEdit": true,
      "changelogId": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "draft": true,
      "feedbackId": 1,
      "productId": 1,
      "scheduled": true,
      "segment": "string",
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `announcement` | boolean |  |
| `canDelete` | boolean |  |
| `canEdit` | boolean |  |
| `changelogId` | number |  |
| `created` | date |  |
| `description` | string |  |
| `draft` | boolean |  |
| `feedbackId` | number |  |
| `productId` | number |  |
| `scheduled` | boolean |  |
| `segment` | string |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Sleekplan API, this operation is `GET /update/:updateid` (base URL `https://api.sleekplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-update.md) for the provider-specific parameters and requirements.

