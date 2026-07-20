# Survalyzer: Delete Members



```
DELETE https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/delete-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Survalyzer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/delete-members?connectionId=$CONNECTION_ID&panelId=1&panelMembersIds%5B%5D=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "panelId": "1",
  "panelMembersIds[]": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/delete-members?${params}`, {
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
| `panelId` | number | yes |  |
| `panelMembersIds[]` | array<number> | yes |  |
| `keepInterviews` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorCode": "string",
      "errorMessage": "string",
      "isSuccess": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorCode` | string |  |
| `errorMessage` | string |  |
| `isSuccess` | boolean |  |

## Native endpoint

Through the native Survalyzer API, this operation is `POST /publicapi/Panel/v3/DeleteMembers` (base URL `https://api.survalyzer-eu.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-members.md) for the provider-specific parameters and requirements.

