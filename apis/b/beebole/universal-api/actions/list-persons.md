# Beebole: List Persons

Retrieves people from your Beebole account.

```
GET https://connect.mindcloud.co/v1/universal/beebole/latest/actions/list-persons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beebole `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beebole/latest/actions/list-persons?connectionId=$CONNECTION_ID&company.id=3" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "company.id": "3"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beebole/latest/actions/list-persons?${params}`, {
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
| `company.id` | number | yes | The Beebole company identifier whose people should be listed. Example: `3`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Beebole API returns.

## Native endpoint

Through the native Beebole API, this operation is `POST` (base URL `https://beebole-apps.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-persons.md) for the provider-specific parameters and requirements.

