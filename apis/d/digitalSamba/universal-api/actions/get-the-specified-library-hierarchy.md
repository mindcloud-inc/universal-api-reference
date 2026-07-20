# Digital Samba: Get the specified library hierarchy

Retrieves a library hierarchy from Digital Samba.

```
GET https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-the-specified-library-hierarchy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digital Samba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-the-specified-library-hierarchy?connectionId=$CONNECTION_ID&library=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "library": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-the-specified-library-hierarchy?${params}`, {
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
| `library` | string | yes | Library path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "externalId": "string",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `externalId` | string |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Digital Samba API, this operation is `GET /libraries/:library/hierarchy` (base URL `https://api.digitalsamba.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-the-specified-library-hierarchy.md) for the provider-specific parameters and requirements.

