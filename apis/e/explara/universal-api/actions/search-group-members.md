# Explara: Search Group Members

Finds group members in Explara by keyword or email.

```
GET https://connect.mindcloud.co/v1/universal/explara/latest/actions/search-group-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Explara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/explara/latest/actions/search-group-members?connectionId=$CONNECTION_ID&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/explara/latest/actions/search-group-members?${params}`, {
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
| `groupId` | string | yes | Explara group identifier. |
| `status` | string | no | Membership status filter, such as active or expired. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Explara API returns.

## Native endpoint

Through the native Explara API, this operation is `POST /cm/api/publisher/search-members` (base URL `https://www.explara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-group-members.md) for the provider-specific parameters and requirements.

