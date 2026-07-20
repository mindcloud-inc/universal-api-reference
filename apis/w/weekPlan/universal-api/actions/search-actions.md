# Week Plan: Search Actions



```
GET https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/search-actions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Week Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/search-actions?connectionId=$CONNECTION_ID&searchText=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "searchText": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/search-actions?${params}`, {
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
| `searchText` | string | yes | Search text used to find matching actions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ActionId": 1,
      "ActionListId": 1,
      "Date": "string",
      "EndDate": "string",
      "HtmlText": "string",
      "IsCompleted": true,
      "IsDeleted": true,
      "Quadrant": 1,
      "RoleId": 1,
      "StartDate": "string",
      "Text": "string",
      "WorkspaceId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ActionId` | number |  |
| `ActionListId` | number |  |
| `Date` | string |  |
| `EndDate` | string |  |
| `HtmlText` | string |  |
| `IsCompleted` | boolean |  |
| `IsDeleted` | boolean |  |
| `Quadrant` | number |  |
| `RoleId` | number |  |
| `StartDate` | string |  |
| `Text` | string |  |
| `WorkspaceId` | number |  |

## Native endpoint

Through the native Week Plan API, this operation is `GET actions/search` (base URL `https://api.weekplan.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-actions.md) for the provider-specific parameters and requirements.

