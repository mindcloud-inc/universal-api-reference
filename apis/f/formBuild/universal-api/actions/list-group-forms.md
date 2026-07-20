# 123FormBuild: List Group Forms

Retrieves forms from a group in 123FormBuilder.

```
GET https://connect.mindcloud.co/v1/universal/formBuild/latest/actions/list-group-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 123FormBuild `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formBuild/latest/actions/list-group-forms?connectionId=$CONNECTION_ID&groupId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formBuild/latest/actions/list-group-forms?${params}`, {
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
| `groupId` | number | yes | The ID of the group |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 123FormBuild API returns.

## Native endpoint

Through the native 123FormBuild API, this operation is `GET /groups/{group_id}/forms` (base URL `https://api.123formbuilder.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-group-forms.md) for the provider-specific parameters and requirements.

