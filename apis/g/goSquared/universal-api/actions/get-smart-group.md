# GoSquared: Get Smart Group

Retrieves a smart group from GoSquared by ID.

```
GET https://connect.mindcloud.co/v1/universal/goSquared/latest/actions/get-smart-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoSquared `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goSquared/latest/actions/get-smart-group?connectionId=$CONNECTION_ID&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goSquared/latest/actions/get-smart-group?${params}`, {
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
| `groupId` | string | yes | The identifier of the Smart Group to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "filters": [
        {}
      ],
      "id": "string",
      "Links": [
        {}
      ],
      "name": "Ava Chen",
      "prefs": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `filters` | array<object> | Provider filter rules that define the smart group. |
| `id` | string | GoSquared smart group identifier. |
| `Links` | array<object> | Provider link metadata returned for related smart group resources. |
| `name` | string | Display name of the smart group. |
| `prefs` | object | Provider preferences returned for the smart group. |

## Native endpoint

Through the native GoSquared API, this operation is `GET people/v1/smartgroups/:groupID` (base URL `https://api.gosquared.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-smart-group.md) for the provider-specific parameters and requirements.

