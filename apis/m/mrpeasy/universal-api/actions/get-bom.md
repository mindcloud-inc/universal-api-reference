# MRPeasy: Get BOM

Retrieves a BOM from MRPeasy.

```
GET https://connect.mindcloud.co/v1/universal/mrpeasy/latest/actions/get-bom
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MRPeasy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mrpeasy/latest/actions/get-bom?connectionId=$CONNECTION_ID&bomId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bomId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mrpeasy/latest/actions/get-bom?${params}`, {
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
| `bomId` | number | yes | MRPeasy BOM ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MRPeasy API returns.

## Native endpoint

Through the native MRPeasy API, this operation is `GET /boms/{{bomId}}` (base URL `https://api.mrpeasy.com/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bom.md) for the provider-specific parameters and requirements.

