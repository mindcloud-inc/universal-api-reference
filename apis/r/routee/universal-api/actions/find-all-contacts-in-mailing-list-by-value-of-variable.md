# Routee: Find all contacts in mailing list by value of variable

Finds all contacts in mailing list by value of variable in Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/find-all-contacts-in-mailing-list-by-value-of-variable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/find-all-contacts-in-mailing-list-by-value-of-variable?connectionId=$CONNECTION_ID&id=1&variableName=Ava%20Chen&searchValue=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1",
  "variableName": "Ava Chen",
  "searchValue": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/find-all-contacts-in-mailing-list-by-value-of-variable?${params}`, {
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
| `id` | number | yes | the ID of the mailing list |
| `variableName` | string | yes | name of variable |
| `searchValue` | string | yes | value of variable |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Routee API returns.

## Native endpoint

Through the native Routee API, this operation is `GET /addressbooks/:id/variables/:variableName/:searchValue` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-all-contacts-in-mailing-list-by-value-of-variable.md) for the provider-specific parameters and requirements.

