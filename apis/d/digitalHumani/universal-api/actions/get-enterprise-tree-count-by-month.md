# Digital Humani: Get Enterprise Tree Count by Month

Retrieves an enterprise's monthly tree count from Digital Humani.

```
GET https://connect.mindcloud.co/v1/universal/digitalHumani/latest/actions/get-enterprise-tree-count-by-month
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digital Humani `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digitalHumani/latest/actions/get-enterprise-tree-count-by-month?connectionId=$CONNECTION_ID&month=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "month": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digitalHumani/latest/actions/get-enterprise-tree-count-by-month?${params}`, {
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
| `month` | string | yes | Month in YYYY-MM format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |

## Native endpoint

Through the native Digital Humani API, this operation is `GET /enterprise/:id/treeCount/:month` (base URL `https://api.digitalhumani.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-enterprise-tree-count-by-month.md) for the provider-specific parameters and requirements.

