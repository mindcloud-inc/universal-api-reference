# Selzy: Get Contact Count

Retrieves the contact count for a Selzy list.

```
GET https://connect.mindcloud.co/v1/universal/selzy/latest/actions/get-contact-count
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Selzy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/selzy/latest/actions/get-contact-count?connectionId=$CONNECTION_ID&listId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/selzy/latest/actions/get-contact-count?${params}`, {
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
| `listId` | number | yes | List code to search within. |
| `params[type]` | string | no | Search contact type: address or phone. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `params[search]` | string | no | Substring to search within email or phone values. |
| `params[tagId]` | number | no | Filter by a specific tag ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {
        "count": 1,
        "listId": 1,
        "searchParams": {
          "type": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result.count` | number |  |
| `result.listId` | number |  |
| `result.searchParams.type` | string |  |

## Native endpoint

Through the native Selzy API, this operation is `POST getContactCount` (base URL `https://api.selzy.com/en/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-count.md) for the provider-specific parameters and requirements.

