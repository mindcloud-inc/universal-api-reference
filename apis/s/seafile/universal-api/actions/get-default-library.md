# Seafile: Get Default Library

Retrieves the default library from Seafile.

```
GET https://connect.mindcloud.co/v1/universal/seafile/latest/actions/get-default-library
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seafile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seafile/latest/actions/get-default-library?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seafile/latest/actions/get-default-library?${params}`, {
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
      "exists": true,
      "repo_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `exists` | boolean |  |
| `repo_id` | string |  |

## Native endpoint

Through the native Seafile API, this operation is `GET https://plus.seafile.com/api2/default-repo/` (base URL `https://plus.seafile.com/api2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-default-library.md) for the provider-specific parameters and requirements.

