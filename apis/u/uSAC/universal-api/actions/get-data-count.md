# USAC: Get Data Count



```
GET https://connect.mindcloud.co/v1/universal/uSAC/latest/actions/get-data-count
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a USAC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uSAC/latest/actions/get-data-count?connectionId=$CONNECTION_ID&resourceId=string&count=count(*)" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resourceId": "string",
  "count": "count(*)"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uSAC/latest/actions/get-data-count?${params}`, {
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
| `resourceId` | string | yes | This is the ID of the dataset, use the List Datasets action to retrieve this. |
| `count` | string | yes | Used similar to SQL where. Docs: https://dev.socrata.com/docs/queries/select Default: `count(*)`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | string |  |

## Native endpoint

Through the native USAC API, this operation is `GET resource/:resourceId.json` (base URL `https://opendata.usac.org/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-data-count.md) for the provider-specific parameters and requirements.

