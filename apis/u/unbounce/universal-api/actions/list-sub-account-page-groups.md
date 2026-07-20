# Unbounce: List Sub Account Page Groups

Retrieves page groups for an Unbounce sub-account.

```
GET https://connect.mindcloud.co/v1/universal/unbounce/latest/actions/list-sub-account-page-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unbounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unbounce/latest/actions/list-sub-account-page-groups?connectionId=$CONNECTION_ID&sub_account_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sub_account_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unbounce/latest/actions/list-sub-account-page-groups?${params}`, {
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
| `sub_account_id` | string | yes | Unbounce sub-account ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metadata": {},
      "pageGroups": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `metadata` | object |  |
| `pageGroups` | array<object> |  |

## Native endpoint

Through the native Unbounce API, this operation is `GET /sub_accounts/:sub_account_id/page_groups` (base URL `https://api.unbounce.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sub-account-page-groups.md) for the provider-specific parameters and requirements.

