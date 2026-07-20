# RollWorks: Get User Attribute Counts by Name and Value

Retrieves user attribute counts in RollWorks by name and value.

```
GET https://connect.mindcloud.co/v1/universal/rollWorks/latest/actions/get-user-attribute-counts-by-name-and-value
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RollWorks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rollWorks/latest/actions/get-user-attribute-counts-by-name-and-value?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rollWorks/latest/actions/get-user-attribute-counts-by-name-and-value?${params}`, {
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
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native RollWorks API, this operation is `POST /audience/v1/user_attribute_counts` (base URL `https://services.adroll.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-attribute-counts-by-name-and-value.md) for the provider-specific parameters and requirements.

