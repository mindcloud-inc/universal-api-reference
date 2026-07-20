# Endear: Get Customers By External IDs



```
GET https://connect.mindcloud.co/v1/universal/endear/latest/actions/get-customers-by-external-ids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Endear `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/endear/latest/actions/get-customers-by-external-ids?connectionId=$CONNECTION_ID&variables.integrationId=string&variables.externalIds%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.integrationId": "string",
  "variables.externalIds[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/endear/latest/actions/get-customers-by-external-ids?${params}`, {
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
| `variables.integrationId` | string | yes | Integration Id for the Endear GraphQL operation. |
| `variables.externalIds[]` | array<string> | yes | External Ids for the Endear GraphQL operation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Endear API, this operation is `POST /graphql` (base URL `https://api.endearhq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customers-by-external-ids.md) for the provider-specific parameters and requirements.

