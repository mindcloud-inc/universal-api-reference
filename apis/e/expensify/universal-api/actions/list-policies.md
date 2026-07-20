# Expensify: List Policies

Retrieves policies from Expensify.

```
GET https://connect.mindcloud.co/v1/universal/expensify/latest/actions/list-policies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Expensify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/expensify/latest/actions/list-policies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/expensify/latest/actions/list-policies?${params}`, {
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
| `adminOnly` | boolean | no | Whether to return only policies where the selected user is an admin. |
| `userEmail` | string | no | Optional user email to gather the policy list for when third-party domain access has been granted. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approvalMode": "string",
      "created": "string",
      "id": "string",
      "name": "Ava Chen",
      "outputCurrency": "string",
      "owner": "string",
      "role": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approvalMode` | string | The approval mode configured for the workspace. |
| `created` | string | When the workspace was created in Expensify. |
| `id` | string | The Expensify policy identifier. |
| `name` | string | The display name of the workspace. |
| `outputCurrency` | string | The default currency for the workspace. |
| `owner` | string | The email address of the workspace owner. |
| `role` | string | The relationship of the selected user to the workspace. |
| `type` | string | The workspace policy type returned by Expensify. |

## Native endpoint

Through the native Expensify API, this operation is `POST ExpensifyIntegrations` (base URL `https://integrations.expensify.com/Integration-Server/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-policies.md) for the provider-specific parameters and requirements.

