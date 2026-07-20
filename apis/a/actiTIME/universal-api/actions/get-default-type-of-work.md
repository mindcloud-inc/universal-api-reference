# actiTIME: Get Default Type of Work

Retrieves the default type of work from actiTIME.

```
GET https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/get-default-type-of-work
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a actiTIME `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/get-default-type-of-work?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/get-default-type-of-work?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "billable": true,
      "default": true,
      "id": 1,
      "name": "Ava Chen",
      "rate": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | Whether the type of work is archived. |
| `billable` | boolean | Whether the type of work is billable. |
| `default` | boolean | Whether the type of work is the default option. |
| `id` | number | Unique type of work identifier. |
| `name` | string | Type of work name. |
| `rate` | number | Hourly rate for the type of work. |

## Native endpoint

Through the native actiTIME API, this operation is `GET /typesOfWork/default` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-default-type-of-work.md) for the provider-specific parameters and requirements.

