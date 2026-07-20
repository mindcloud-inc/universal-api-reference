# Xata: Get available instance types



```
GET https://connect.mindcloud.co/v1/universal/xata/latest/actions/list-instance-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xata/latest/actions/list-instance-types?connectionId=$CONNECTION_ID&organizationID=string&region=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationID": "string",
  "region": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xata/latest/actions/list-instance-types?${params}`, {
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
| `organizationID` | string | yes | Unique identifier of the organization to check instance type availability for |
| `region` | string | yes | Region to check instance type availability for |

## Response

```json
{
  "success": true,
  "data": [
    {
      "instanceTypes": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `instanceTypes` | array<object> | Array of available instance types with their properties |

## Native endpoint

Through the native Xata API, this operation is `GET /organizations/:organizationID/instanceTypes` (base URL `https://api.xata.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-instance-types.md) for the provider-specific parameters and requirements.

